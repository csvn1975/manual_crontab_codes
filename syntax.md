#!/bin/bash

# variable
x="das ist definition eine variable, die darf ohne leerzeichen sein."
y="darf nie mal leerzeichen"

a=151
b=10
z=$(($a+$b))

echo $x
echo $y
echo $(($a+$b))
echo $z 

# if-syntax:
echo "======= if-syntax: VORSICHT leerzeichen =========="
if [ $a = 5 ]; then
    echo "value a is 5"
elif [ $a -le 10 ]; then
    echo "value a is less 10"

elif [ $a -gt 20 ] && [ $b = 10 ]; then
    echo "value a is greater 20 and b is 10"

elif [ $a -gt 20 ]; then
    echo "value a is greater 20"

else 
    echo "value a is between 10 and 20"
fi

# loop
echo "======= loop  =========="