# PL Project: Control Flow Graphs Generator

Nandakishore S Menon | IMT2019057 \
Rachna S Kedigehalli | IMT2019069 \
Yashovardhan Reddy | IMT2019097 \
Lalith Kumar Reddy G | IMT2019509 \

#

## Problem Description

It is difficult to comprehend the behavior of a program from its source code. It is important to know how a program behaves in different situations in order to prevent errors, crashes and other unexpected runtime behavior. Information about the behaviour of the program can be extracted with static analysis of the code, i.e. by drawing its **control flow graph**, which outlines all possible paths that might be traversed when the program is executed. 

However, doing so by hand can become taxing for large and complex programs and is prone to errors. This tool draws control flow graphs given syntactically correct programs (compiles without errors).

Consider for the following piece of code:
```C
{
    int x = 0 ;
    int y = 0 ;
    for(int i=0; i<5;i++) {
        if ( x < i ) {
            x++;
        }
        else {
            y++;
        }
    }
    x=x+y;
}
```
Corresponding control flow graph generated by CFG_Gen would be:
![CFG Example](/images/example.png "CFG Example")

## Instructions to use the CFG Generator
To install dependencies and build the executable:
```
make install
```
Run it with a compilable C source code:
```
cfg_gen < sample.c
```
To convert the .dot files generated to .png:
```
./dot_to_img.sh
```


## References
[A Control Flow Graph Generator for Java Code](https://theses.liacs.nl/pdf/DavidDeMuinickKeizer.pdf)

