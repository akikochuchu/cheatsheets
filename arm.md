##Branching (BL, BX, BLX) 

http://infocenter.arm.com/help/index.jsp?topic=/com.arm.doc.dui0204j/Cihfddaf.html

- The ```BL``` and ```BLX``` instructions copy the address of the next instruction into ```LR (R14)```
- The ```BX``` and ```BLX`` instructions can change the processor state from ARM to Thumb, or vice versus
- ```BLX``` always changes the state

```0000bf18   blx   r2```

## Multiple Register Data Tranfer

```LDMIA r0, {r3, r7}```

- Load words addressed by ```r0``` into ```r3```, and ```r7```
- Increment after each load

```STM r1, {r6 - r8}```

- Store ``r6, r7, r8`` into words addressed by ```r1```
- Write back the final address into ```r1```
- Decrement before each store

