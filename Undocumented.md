# **Undocumented Instructions** #

A list of all the undocumented instructions supported by the emulator. These are not guaranteed to exist in every processor but they where common enough to be used in real software.


```
  #DD #24      INC  IXH           #FD #24       INC  IYH
  #DD #25      DEC  IXH           #FD #25       DEC  IYH
  #DD #26 nn   LD   IXH,nn        #FD #26 nn    LD   IYH,nn
  #DD #2C      INC  IXL           #FD #2C       INC  IYL
  #DD #2D      DEC  IXL           #FD #2D       DEC  IYL
  #DD #2E nn   LD   IXL,nn        #FD #2E nn    LD   IYL,nn
  #DD #44      LD   B,IXH         #FD #44       LD   B,IYH
  #DD #45      LD   B,IXL         #FD #45       LD   B,IYL
  #DD #4C      LD   C,IXH         #FD #4C       LD   C,IYH
  #DD #4D      LD   C,IXL         #FD #4D       LD   C,IYL
  #DD #54      LD   D,IXH         #FD #54       LD   D,IYH
  #DD #55      LD   D,IXL         #FD #55       LD   D,IYL
  #DD #5C      LD   E,IXH         #FD #5C       LD   E,IYH
  #DD #5D      LD   E,IXL         #FD #5D       LD   E,IYL
  #DD #60      LD   IXH,B         #FD #60       LD   IYH,B
  #DD #61      LD   IXH,C         #FD #61       LD   IYH,C
  #DD #62      LD   IXH,D         #FD #62       LD   IYH,D
  #DD #63      LD   IXH,E         #FD #63       LD   IYH,E
  #DD #64      LD   IXH,IXH       #FD #64       LD   IYH,IYH
  #DD #65      LD   IXH,IXL       #FD #65       LD   IYH,IYL
  #DD #67      LD   IXH,A         #FD #67       LD   IYH,A
  #DD #68      LD   IXL,B         #FD #68       LD   IYL,B
  #DD #69      LD   IXL,C         #FD #69       LD   IYL,C
  #DD #6A      LD   IXL,D         #FD #6A       LD   IYL,D
  #DD #6B      LD   IXL,E         #FD #6B       LD   IYL,E
  #DD #6C      LD   IXL,IXH       #FD #6C       LD   IYL,IYH
  #DD #6D      LD   IXL,IXL       #FD #6D       LD   IYL,IYL
  #DD #6F      LD   IXL,A         #FD #6F       LD   IYL,A
  #DD #7C      LD   A,IXH         #FD #7C       LD   A,IYH
  #DD #7D      LD   A,IXL         #FD #7D       LD   A,IYL
  #DD #84      ADD  A,IXH         #FD #84       ADD  A,IYH
  #DD #85      ADD  A,IXL         #FD #85       ADD  A,IYL
  #DD #8C      ADC  A,IXH         #FD #8C       ADC  A,IYH
  #DD #8D      ADC  A,IXL         #FD #8D       ADC  A,IYL
  #DD #94      SUB  IXH           #FD #94       SUB  IYH
  #DD #95      SUB  IXL           #FD #95       SUB  IYL
  #DD #9C      SBC  A,IXH         #FD #9C       SBC  A,IYH
  #DD #9D      SBC  A,IXL         #FD #9D       SBC  A,IYL
  #DD #A4      AND  IXH           #FD #A4       AND  IYH
  #DD #A5      AND  IXL           #FD #A5       AND  IYL
  #DD #AC      XOR  IXH           #FD #AC       XOR  IYH
  #DD #AD      XOR  IXL           #FD #AD       XOR  IYL
  #DD #B4      OR   IXH           #FD #B4       OR   IYH
  #DD #B5      OR   IXL           #FD #B5       OR   IYL
  #DD #BC      CP   IXH           #FD #BC       CP   IYH
  #DD #BD      CP   IXL           #FD #BD       CP   IYL
  
  #DD #CB nn #00   RLC  (IX+nn)   &  LD   B,(IX+nn)      
  #DD #CB nn #01   RLC  (IX+nn)   &  LD   C,(IX+nn)
  #DD #CB nn #02   RLC  (IX+nn)   &  LD   D,(IX+nn)
  #DD #CB nn #03   RLC  (IX+nn)   &  LD   E,(IX+nn)
  #DD #CB nn #04   RLC  (IX+nn)   &  LD   H,(IX+nn)
  #DD #CB nn #05   RLC  (IX+nn)   &  LD   L,(IX+nn)
  #DD #CB nn #06   RLC  (IX+nn)   &  LD   F,(IX+nn)         
  #DD #CB nn #07   RLC  (IX+nn)   &  LD   A,(IX+nn)

  #DD #CB nn #08   RRC  (IX+nn)   &  LD   B,(IX+nn) 
  #DD #CB nn #10   RL   (IX+nn)   &  LD   B,(IX+nn) 
  #DD #CB nn #18   RR   (IX+nn)   &  LD   B,(IX+nn) 
  #DD #CB nn #20   SLA  (IX+nn)   &  LD   B,(IX+nn) 
  #DD #CB nn #28   SRA  (IX+nn)   &  LD   B,(IX+nn) 
  #DD #CB nn #30   SLL  (IX+nn)   &  LD   B,(IX+nn)   
  #DD #CB nn #38   SRL  (IX+nn)   &  LD   B,(IX+nn) 
  #DD #CB nn #80   RES  0,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #88   RES  1,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #90   RES  2,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #98   RES  3,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #A0   RES  4,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #A8   RES  5,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #B0   RES  6,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #B8   RES  7,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #C0   SET  0,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #C8   SET  1,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #D0   SET  2,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #D8   SET  3,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #E0   SET  4,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #E8   SET  5,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #F0   SET  6,(IX+nn) &  LD   B,(IX+nn) 
  #DD #CB nn #F8   SET  7,(IX+nn) &  LD   B,(IX+nn)

  #CB #30          SLL  B                                   
  #CB #31          SLL  C
  #CB #32          SLL  D
  #CB #33          SLL  E
  #CB #34          SLL  H
  #CB #35          SLL  L
  #CB #36          SLL  (HL)
  #CB #37          SLL  A

  #ED #70          IN   F,(C)                               
  #ED #71          OUT  F,(C) 

```