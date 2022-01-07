Module 5 : Shell Scripts 

-----------------------------------------

Topics : 
+ Study of Shell, Types of Shell, Variables andOperators
+ Write a shell script to perform arithmetic operations
+ Write a shell script to calculate simple interest
+ Write a shell script to determine largest among three integer numbers
+ Write a shell script to determine a given year is
leap year or not
+ Write a shell script to print multiplication table of
given number using while statement
+ Write a shell script to search whether element is
present is in the list or not
+ Write a shell script to compare two strings
+ Write a shell script to read and check if the directory / file exists or not, if not make the directory / file
+ Write a shell script to implement menu-driven calculator using case statement.
+ Write a shell script to print following pattern:

  \*

  \* \*

  \* \* \* \*

  \* \* \* \* \* 



---------------------------------------


# 1. Shell Script to perform Arithmatic Operations using expr

    #!/bin/sh

    a=10
    b=20

    val=`expr $a + $b`
    echo "a + b : $val"

    val=`expr $a - $b`
    echo "a - b : $val"

    val=`expr $a \* $b`
    echo "a * b : $val"

    val=`expr $b / $a`
    echo "b / a : $val"

    val=`expr $b % $a`
    echo "b % a : $val"

    if [ $a == $b ]
    then
      echo "a is equal to b"
    fi

    if [ $a != $b ]
    then
      echo "a is not equal to b"
    fi


# 2. Shell Script to perform Arithmatic Operations using Double Parenthesis


    #!/bin/bash
    
    x=10
    y=3
    
    echo $(( x + y ))   # addition
    echo $(( $x + $y )) # also valid
    
    echo $(( x - y ))   # subtraction
    echo $(( $x - $y )) # also valid
    
    echo $(( x * y ))   # multiplication
    echo $(( $x * $y )) # also valid
    
    echo $(( x / y ))   # division
    echo $(( $x / $y )) # also valid
    
    echo $(( x ** y ))  # exponentiation
    echo $(( $x ** $y ))    # also valid
    
    echo $(( x % y ))   # modular division
    echo $(( $x % $y )) # also valid
    
    (( x += 4 ))    # increment variable by constant
    echo $x
    
    (( x -= 4 ))    # decrement variable by constant 
    echo $x
    
    (( x *= 4 ))    # mulitply variable by constant
    echo $x
    
    (( x /= 4 ))    # divide variable by constant
    echo $x
    
    (( x %= 4 ))    # Remainder of Dividing Variable by Constant
    echo $x



# 3. Shell Script to perform Arithmatic Operations using let


    #!/bin/bash
    
    x=10
    y=3
    z=0
    
    let "z = $(( x + y ))"  # addition
    let z=$((x+y))  # also valid without double quotes when no spaces in expression
    echo $z
    
    let "z = $(( x - y ))"  # subtraction
    let z=$((x-y))
    echo $z
    
    let "z = $(( x * y ))"  # multiplication
    let z=$((x*y))
    echo $z
    
    let "z = $(( x / y ))"  # division
    let z=$((x/y))
    echo $z
    
    let "z = $(( x ** y ))" # exponentiation
    let z=$((x**y))
    echo $z
    
    let "z = $(( x % y ))"  # modular division
    let z=$((x%y))
    echo $z
    
    let "x += 4"    # increment variable by constant
    echo $x
    
    let "x -= 4"    # decrement variable by constant 
    echo $x
    
    let "x *= 4"    # mulitply variable by constant
    echo $x
    
    let "x /= 4"    # divide variable by constant
    echo $x
    
    let "x %= 4"    # Remainder of Dividing Variable by Constant
    echo $x


# 4. Write a shell script to calculate simple interest

    echo " Enter the principle value: "
    read p
    echo " Enter the rate of interest:"
    read r
    echo " Enter the time period:"
    read t
    s=`expr $p \* $t \* $r / 100`
    echo " The simple interest is "
    echo $s

# 5. Write a shell script to determine largest among three integer numbers

    echo "Enter the 1st Number: "
    read n1
    echo "Enter the 2nd Number: "
    read n2
    echo "Enter the 3rd Number: "
    read n3

    total=`expr $n1 + $n2 + $n3`
    avg=`expr $total / 3`

    if [ $n1 -gt $n2 -a $n1 -gt $n3 ]
    then
    echo "$n1 is the Largest of three"
    elif [ $n2 -gt $n1 -a $n2 -gt $n3 ]
    then
    echo "$n2 is the Largest of three"
    elif [ $n3 -gt $n1 -a $n3 -gt $n2 ]
    then
    echo "$n3 is the Largest of three"
    else
    echo "All the three numbers are Equal"
    fi
    echo "Total: $total"
    echo "Average: $avg"

# 6.  Write a shell script to determine a given year is leap year or not


    echo "Enter the year in 4 digits: "
    read num
    if [ $num -ge 1000 -a $num -le 9999 ]
    then
    if [ `expr $num % 4` -eq 0 ]
    then
    echo "The year $num is a Leap year"
    else
    echo "The year $num is not a Leap year"
    fi
    else
    echo "Invalid year format"
    fi


### Lab Questions and Tasks (Total 25 Marks ) 
