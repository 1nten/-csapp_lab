## bomb

phase_1（）

```assembly
400e37:   48 89 c7                mov    %rax,%rdi    //第一个参数  
400e3a:   e8 a1 00 00 00          callq  400ee0 <phase_1>
...
0x0000000000400ee0 <+0>:    sub    $0x8,%rsp 
0x0000000000400ee4 <+4>:    mov    $0x402400,%esi   //第二个参数
0x0000000000400ee9 <+9>:    callq  0x401338 <strings_not_equal>
```

让参数一，二相等即可

Border relations with Canada have never been better.



phase_2（）

利用callq 0x40145c <read_six_numbers>确定字符串格式，

利用0000000000400F1A   add     eax, eax让后边的数翻倍

字符串为“1 2 4 8 16 32”

phase_3（）

尝试分析时，发现jcc指令经常弄混，又回去复习了一遍

cmp oprd1,oprd2 + JNBE/JA 无符号

cmp oprd1,oprd2 + JNLE/JG 有符号

oprd1>oprd2时跳转

JZ/JE 相等则跳转

    0 207  ===》x/x (int *)0x402470 打印得到地址400f7c
    1 311  ===》x/x (int *)0x402478 打印得到地址400fb9
    2 707  ===》x/x (int *)0x402480 打印得到地址400f83
    3 256  ===》x/x (int *)0x402488 打印得到地址400f8a
    4 389  ===》x/x (int *)0x402490 打印得到地址400f91
    5 206  ===》x/x (int *)0x402498 打印得到地址400f98
    6 682  ===》x/x (int *)0x4024a0 打印得到地址400f9f
    7 327  ===》x/x (int *)0x4024a8 打印得到地址400fa6

