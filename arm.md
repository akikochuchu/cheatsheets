##Registers

- ```r0```  - arg / scratch / result
- ```r1```  - arg / scratch / result
- ```r2```  - arg / scratch / result
- ```r3```  - arg / sratch  / result
- ```r4```  - register var
- ```r5```  - register var
- ```r6```  - register var
- ```r7```  - register var
- ```r8```  - register var
- ```r9```  - stack base
- ```r10``` - stack limit / stack chunk handle / register var
- ```r11``` - frame pointer
- ```r12``` - ip
- ```r13``` - stack pointer
- ```r14``` - link register
- ```r15``` - program counter

##Branching - ```BL, BX, BLX```

http://infocenter.arm.com/help/index.jsp?topic=/com.arm.doc.dui0204j/Cihfddaf.html

- The ```BL``` and ```BLX``` instructions copy the address of the next instruction into ```LR (R14)```
- The ```BX``` and ```BLX``` instructions can change the processor state from ARM to Thumb, or vice versus
- ```BLX``` always changes the state

```0000bf18   blx   r2```

## Multiple Register Data Transfer

```nasm
LDMIA r0, {r3, r7}
```

- Load words addressed by ```r0``` into ```r3```, and ```r7```
- Increment after each load

```nasm
STM r1, {r6 - r8}
```

- Store ``r6, r7, r8`` into words addressed by ```r1```
- Write back the final address into ```r1```
- Decrement before each store


## Memory Addressing

Each addressing mode includes a base memory address and an offset in bytes.

###Pre-Index

**Format**

```nasm
LDR r1, [r0, #4]

r0 = 0x4000000 + 4 (0x40000004)
r1 = content at 0x40000004
r0 remains unchanged

```

