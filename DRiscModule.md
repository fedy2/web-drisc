# Introduction #

The DRisc module contains the compiler, the assembler and the virtual machine code. The supported DRisc language is described [here](http://backus.di.unipi.it/~marcod/wiki/doku.php?id=drisc)

# Details #

![http://wiki.web-drisc.googlecode.com/git/drisc.png](http://wiki.web-drisc.googlecode.com/git/drisc.png)

  1. The **compiler** uses a regular expression in order to retrieve all the statement components:
```
   [label:] instruction [par1] [par2] [par3] [par4]
```
> > For example:
```
   loop: ld R2, R1, R10
```
  1. The assembler calculates all the instructions offsets, the initial instruction and filter out the memory and registry directives
  1. The virtual machine is able to run the assembled program both step by step or in a whole execution.

# Source Code #
The module source code can be found [here](http://code.google.com/p/web-drisc/source/checkout?repo=drisc)