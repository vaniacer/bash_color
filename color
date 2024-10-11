#!/bin/bash
#--------------------------------------------------------------------+
#Color picker, usage: printf $BLD$CUR$RED$BBLU'Hello World!'$DEF     |
#-------------------------+--------------------------------+---------+
#       Text color        |       Background color         |         |
#-----------+-------------+--------------+-----------------+         |
# Base color|Lighter shade| Base color   | Lighter shade   |         |
#-----------+-------------+--------------+-----------------+         |
BLK='\e[30m'; blk='\e[90m'; BBLK='\e[40m'; bblk='\e[100m' #| Black   |
RED='\e[31m'; red='\e[91m'; BRED='\e[41m'; bred='\e[101m' #| Red     |
GRN='\e[32m'; grn='\e[92m'; BGRN='\e[42m'; bgrn='\e[102m' #| Green   |
YLW='\e[33m'; ylw='\e[93m'; BYLW='\e[43m'; bylw='\e[103m' #| Yellow  |
BLU='\e[34m'; blu='\e[94m'; BBLU='\e[44m'; bblu='\e[104m' #| Blue    |
MGN='\e[35m'; mgn='\e[95m'; BMGN='\e[45m'; bmgn='\e[105m' #| Magenta |
CYN='\e[36m'; cyn='\e[96m'; BCYN='\e[46m'; bcyn='\e[106m' #| Cyan    |
WHT='\e[37m'; wht='\e[97m'; BWHT='\e[47m'; bwht='\e[107m' #| White   |
#-------------------------{ Effects }----------------------+---------+
DEF='\e[0m'   #Default color and effects                             |
BLD='\e[1m'   #Bold\brighter                                         |
DIM='\e[2m'   #Dim\darker                                            |
CUR='\e[3m'   #Italic font                                           |
UND='\e[4m'   #Underline                                             |
INV='\e[7m'   #Inverted                                              |
COF='\e[?25l' #Cursor Off                                            |
CON='\e[?25h' #Cursor On                                             |
#------------------------{ Functions }-------------------------------+
# Text positioning, usage: XY 10 10 'Hello World!'                   |
XY(){ printf "\e[$2;${1}H$3"; }                                     #|
# Print line, usage: line - 10 | line -= 20 | line 'Hello World!' 20 |
line(){ printf -v _L %$2s; printf -- "${_L// /$1}"; }               #|
# Create sequence like {0..(X-1)}, usage: que 10                     |
que(){ printf -v _N %$1s; _N=(${_N// / 1}); printf "${!_N[*]}"; }   #|
#--------------------------------------------------------------------+
# loops are better on large scales like 20000+ but fail on 1000 or less
# line(){ for ((i=0; i<$2; i++)); { printf -- '%s' "$1"; }
# que(){ printf 0; for ((i=1; i<$1; i++)); { printf -- " %s" $i; }
