1. Explain in your own words and examples, what is Shell Scripting for DevOps.
2. What is #!/bin/bash? can we write #!/bin/sh as well?

3. Write a Shell Script which prints I will complete #90DaysOofDevOps challenge
#!/bin/bash
echo "I will complete #90DaysOofDevOps challenge"
:wq

4. Write a Shell Script to take user input, input from arguments and print the variables.
#!/bin/bash
echo "Enter a number"
read var1
echo "The number is $var1"

5. Write an Example of If else in Shell Scripting by comparing 2 numbers
#!/bin/bash
echo "Enter the first number"
read var1
echo "Enter the second number"
read var2
if [ "$var1" -eq "$var2" ] ;
then
echo "The first number is equals to the second number"
elif [ "$var1" -gt "$var2" ] ;
then
echo "The first number is greater than the second number"
else
echo "The first number is smaller than the second number"
fi


