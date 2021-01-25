#
 16 registers . R0-R15.
 
 R15 = stack pointer.

#
opcodes

| Name      | Description | Args | Size | OP |
| ----------- | ---------- | - | - | - |
| NOP      | No OPeration      | | 1 | 0x00 |
|  |  | | |
| RTS      | Return From Sub   | | 1 | 0x?? |
|  |  | | |
| INC     | Increment Register Ra   | Ra | 2 | 0x?? |
| DEC     | Decrement Register Ra   | Ra | 2 | 0x?? |
|  |  | | |
| MOV      | store Ra in Rb | Ra,Rb  | 2 | 0x?? |
| MOV      | store Ra in Memory pointed to by Rb | Ra,[Rb]   | 2 | 0x?? |
| MOV      | Memory pointed to by Ra in Rb  | [Ra],Rb  | 2 | 0x?? |
| MOV      | store Ra in Memory pointed to by (Rb + Rc) | Ra,[Rb:Rc]   | 2 | 0x?? |
| MOV      | Memory pointed to by (Ra+Rb) in Rc  | [Ra:Rb],Rc  | 2 | 0x?? |
| MOV      | Immediate value into Ra  | #Value,Ra  | 6 | 0x?? |
| MOV      | Contents of memory into Ra  | Memory,Ra  | 6 | 0x?? |
| MOV      | Memory pointed to by Ra to Memory  | [Ra],Memory  | 6 | 0x?? |
| MOV      | Memory pointed to by (Ra+Rb) to Memory  | [Ra:Rb],Memory  | 6 | 0x?? |
|  |  | | |
| ALU |Only operates on Registers  |
|  |  | | |
| ADD | Add Ra to Rb | Ra,Rb | 2 | 
| SUB | Subtract Ra from Rb | Ra,Rb | 2 | 
| AND | And Rb with Ra | Ra,Rb | 2 | 
| OR | Or Rb with Ra | Ra,Rb | 2 | 
| NOT | Not Rb with Ra | Ra,Rb | 2 | 
| XOR | eXclusive Or Rb with Ra | Ra,Rb | 2 | 
|  |  | | |
| CMP | Compare Register Ra with Rb | Ra,Rb | |
|  |  | | |
| BRA | Branch Always to address in Ra | [Ra] | 2 |
| BRA | Branch Always to absolute address  | $ffffffff | 5 |
| BSR | Branch Subroutine to address in Ra | [Ra] | 2 |
| BSR | Branch Subroutine to absolute address  | $ffffffff | 5 |
| BEQ | Branch flag == to address in Ra | [Ra] | 2 |
| BEQ | Branch flag == to absolute address  | $ffffffff | 5 |
| BNE | Branch flag != to address in Ra | [Ra] | 2 |
| BNE | Branch flag != to absolute address  | $ffffffff | 5 |
| BLS | Branch sign flag < to address in Ra | [Ra] | 2 |
| BLS | Branch sign flag < to absolute address  | $ffffffff | 5 |
| BGT | Branch sign flag > to address in Ra | [Ra] | 2 |
| BGT | Branch sign flag > to absolute address  | $ffffffff | 5 |



