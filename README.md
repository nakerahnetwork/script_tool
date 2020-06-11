# script_tool
* script tool pyhton2.7 
* script take input as option and arguments
## how to use 
* git clone https://github.com/jac11/script_tool.git
* chmod +x script.py
* to check all  option open help menu by typing ./script.py -h or --help
* follow the help menu to use option 
## help menu overview
``` usage: script.py [-h] [-c] [-r] [-a] [-A] [-H] [-l] [-s] [-G] [-F] [-D]

Usage: [OPtion] [arguments] [length] [arguments] Exsample: -c a -l 300

optional arguments:
  -h, --help         show this help message and exit
  -c , --char        to generate A or B..etc char Exsample : -c a -l 220
  -r , --random      to gentreta random pattern Exsample : -r r -l 200
  -a , --alfa        to generate AAAAtoZZZZ 32bit Exsample : -a x86 -l 26
  -A , --alfa_64     generate AAAAAAAAtoZZZZZZZZ 64bit Exsample :-A x64 -l 26
  -H , --Hexdecode   to decode hex address Exampel: -H 0x00000000
  -l , --length      to give length of the pattern
  -s , --L_endian    to little-endian struct EExsample: -s 0x0876bf67
  -G , --libc        to grep from libc Library Exsample -G /bin/sh
  -F , --object      Select program dump Exsample: -F program.o -D ret
  -D , --dump        grep program addresses Exsample: -F Program -D pop
```
### [Return-to-libc]
* to grep from libc library use ./script.py -G /bin/sh # -G option grep folow with the string 
* ```~/script_tool# ./script.py -G /bin/sh```
* ```grep _from _libc:  188406 /bin/sh```
### [Return-oriented programming ROP]
* to grep pop ,ret from the program use -F and - D

``` 
~/script_tool# ./script.py  -F stack7 -D ret

 8048383:	c3                   	ret    
 8048494:	c3                   	ret    
 80484c2:	c3                   	ret    
 8048544:	c3                   	ret    
 8048553:	c3                   	ret    
 8048564:	c3                   	ret    
 80485c9:	c3                   	ret    
 80485cd:	c3                   	ret    
 80485f9:	c3                   	ret    
 8048617:	c3                   	ret    
```




