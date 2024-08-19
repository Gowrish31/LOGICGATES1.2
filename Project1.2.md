And.hdl 
CHIP And {
    IN a, b;
    OUT out;


    PARTS:
    Nand(a=a,b=b,out=nandout);
    Not(in=nandout,out=out);
}
![image](https://github.com/user-attachments/assets/94a9b955-e7ad-4ed0-8454-41dabb3a90ac)

Xor.hdl
CHIP Xor {
    IN a, b;
    OUT out;

    PARTS:
    Not(in=a,out=nota);
    Not(in=b,out=notb);
    And(a=nota,b=b,out=t1);
    And(a=a,b=notb,out=t2);
    Or(a=t1,b=t2,out=out);
}
![image](https://github.com/user-attachments/assets/47ba4a3f-5c8a-4c6e-98d5-6a7265614fb8)

