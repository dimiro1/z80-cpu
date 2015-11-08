# **Create A Machine** #

```

How to create a simple machine and execute an instruction.  After that, the rest is up to you !

Lets Implement …

Minimal i/o implementation. Any data written to an output port is converted to a character and written to the terminal. All input returns zero.

	
/**
 * Very simple I/O implementation
 */
import net.sleepymouse.microprocessor.IBaseDevice;
 
public class Z80IO implements IBaseDevice
{
    /**
     * Do nothing
     */
    @Override
    public int IORead(int address)
    {
        return 0;
    }
 
    /**
     * Print a character
     */
    @Override
    public void IOWrite(int address, int data)
    {
        System.out.print((char) data);
    }
}



Minimal memory implementation. Just a few bytes of code and data down at address zero. Writes do nothing.

	
/**
 * Very simple memory implementation
 */
import net.sleepymouse.microprocessor.IMemory;
 
public class Z80Memory implements IMemory
{
    int[]   memory  = new int[] {
                        0x21, 0x0C, 0x00, // ld hl, 0008
            0x06, 0x0F, // ld b,0f
            0x7e, // ld a,(hl)
            0x23, // inc hl
            0xD3, 0x00, // out (00), a
            0x10, 0xFA, // djnz
            0x76, // halt
            0x48, 0x65, 0x6C, 0x6C, 0x6F, // Message ASCII
            0x20, 0x77, 0x6F, 0x72, 0x6C, //
            0x64, 0x21, 0x20, 0x0D, 0x0A };
 
    @Override
    // Read a byte from meory
    public int readByte(int address)
    {
        return memory[address];
    }
 
    @Override
    // Read a word from memory
    public int readWord(int address)
    {
        return readByte(address) + readByte(address + 1)*256;
    }
 
    @Override
    public void writeByte(int address, int data)
    {}
 
    @Override
    public void writeWord(int address, int data)
    {}
}



Now we have memory and i/o, all we need is a processor to do some work.

	
/**
 * Very simple Z80 computer
 */
import net.sleepymouse.microprocessor.ProcessorException;
import net.sleepymouse.microprocessor.Z80.Z80Core;
 
public class Z80Demo
{
    /**
     * Create CPU and run a program
     */
    public static void main(String[] args)
    {
        Z80Demo z80Demo = new Z80Demo();
        z80Demo.run();
    }
 
    // Create CPU and loop through program
    public void run()
    {
        Z80Core z80 = new Z80Core(new Z80Memory(),
                                          new Z80IO());
        z80.reset();
        while (!z80.getHalt())
        {
            try
            {
                z80.executeOneInstruction();
            }
            catch (ProcessorException e)
            {
                System.out.println("Hardware crash, oops! "
                                   + e.getMessage());
            }
        }
    }
}

```

Well, wasn’t that simple ? I leave it as an exercise to the reader to put together that uber S-100 CP/M-80 system that you always wanted but you (your parents ?) could not afford.