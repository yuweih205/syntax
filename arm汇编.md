SME mova q时是跳行mova 有十六个zaq 取得是同个za的 但za是za0 za1 za2……za16排列的
p寄存器是sve/8 8是mini operate width p也可以交织



内联汇编

clang 

```
asm volatile(
""
:[变量名]"r"（变量名） //outputs
: //inputs
:"mem","cc") //clobbers
```

r是register的缩写 

+r 输入输出 值会被改

 =r 仅用于输出  编译器可以决定

 -r仅用于输出 值会被改



