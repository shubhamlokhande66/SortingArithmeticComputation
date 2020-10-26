#!/bin/bash

declare -A result
declare -a array

echo "Welcome to Arithmetic Computation & Sorting Computation"

echo -n "Enter 1st number"
read firstInput
echo -n "Enter 2nd number"
read secondInput
echo -n "Enter 3rd number"
read thirdInput

#Compute first arithematic operation
firstResult=`echo "scale=2;$firstInput + $secondInput * $thirdInput" | bc -l`
#echo $firstResult

#Compute second arithematic operation
secondResult=`echo "scale=2;$firstInput * $secondInput + $thirdInput" | bc -l`
#echo $secondResult

#Compute third arithematic operation
thirdResult=`echo "scale=2;$thirdInput + $firstInput / $secondInput" | bc -l`
#echo $thirdResult

#Compute Fourth arithematic operation
fourthResult=`echo "scale=2;$firstInput % $secondInput + $thirdInput" | bc -l`
#echo $fourthResult

#Storing result in result using dictionary
result[1]=$firstResult
result[2]=$secondResult
result[3]=$thirdResult
result[4]=$fourthResult

#reading values from result to array
length="${#result[@]}"
for ((index1=0; $index1<$length; index1++))
do
   array[index1]=${result[$((index1+1))]}
done
echo "array:${array[@]}"

#Sorted result in descending order
 length1="${#array[@]}"
   for (( i=0; i<$length1; i++ ))
   do
      for (( j=0; j<$length1-1; j++ ))
      do
         if (( $(echo "${array[j]} < ${array[j+1]}" |bc -l) ))
         then
            temp=${array[j]}
            array[j]=${array[j+1]}
            array[j+1]=$temp
         fi
      done
   done
echo "Sorted in descending:"${array[@]}

#sorted result in ascending order
length1="${#array[@]}"
   for (( i=0; i<$length1; i++ ))
   do
      for (( j=0; j<$length1-1; j++ ))
      do
         if (( $(echo "${array[j]} > ${array[j+1]}" |bc -l) ))
         then
            temp=${array[j]}
            array[j]=${array[j+1]}
            array[j+1]=$temp
         fi
      done
   done
echo "Sorted the values - ascending order: ${array[@]}"
