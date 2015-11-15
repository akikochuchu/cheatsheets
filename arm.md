##Branching (BL, BX, BLX) 

http://infocenter.arm.com/help/index.jsp?topic=/com.arm.doc.dui0204j/Cihfddaf.html

- The ```BL``` and ```BLX``` instructions copy the address of the next instruction into ```LR (R14)```
- The ```BX``` and ```BLX`` instructions can change the processor state from ARM to Thumb, or vice versus
- ```BLX``` always changes the state

```0000bf18   blx   r2```


