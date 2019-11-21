# PROGRAMMING FOR PROBLEM SOLVING

## **_ESC-18104/18105_**

###  **_PRACTICAL FILE_**

### **SUBMITTED BY**

#### **NAME:-**_SHIV PRATAP DUBEY_

#### **ROLL NO.:-** _1914105_

#### **DEPARTMENT:-**_CIVIL_

#### **SECTION:-** _B2_

### **SUBMITTED TO:-**

#### _ASST.PROFESSOR MISS YADVIR KAUR_

![logo](https://github.com/Shiv2ubey786/PRACTICA-FILE.md/blob/master/logo.jpg)

 # List of programs
### 1.Addition of two integers
    #include<stdio.h>
    int main()
    {
    int First No., Second No., Sum of two No.;
    printf("\nEnter two no: ");
    scanf("%d %d", &First No, &Second No);
    Sum of two No. = First No.+ Second No. ;
    printf("Sum of two No. : %d",Sum of two No.);
    return(0);
    }
### 2. Write a C Program to Multiply two Floating Point Numbers
    #include <stdio.h>
    int main()
    {
        double firstNumber, secondNumber, product;
        printf("Enter two numbers: ");
        // Stores two floating point numbers in variable firstNumber and secondNumber respectively
        scanf("%lf %lf", &firstNumber, &secondNumber);  
     
        // Performs multiplication and stores the result in variable productOfTwoNumbers
        product = firstNumber * secondNumber;  
        // Result up to 2 decimal point is displayed using %.2lf
        printf("Product = %.2lf", product);
        
        return 0;
    }
### 3. Write a C Program to Check Whether a Number is Even or Odd using if else statement.
    #include <stdio.h>
    int main()
    {
        int number;
        printf("Enter an integer: ");
        scanf("%d", &number);
        // True if the number is perfectly divisible by 2
        if(number % 2 == 0)
            printf("%d is even.", number);
        else
            printf("%d is odd.", number);
        return 0;
    }
  ### 4. Write a C Program to calculate the sum of first 10 natural numbers using for loop.
  
    #include <stdio.h>
     int main()
     {
      int  j, sum = 0;

    printf("The first 10 natural number is :\n");
 
    for (j = 1; j <= 10; j++)
    {
        sum = sum + j;
        printf("%d ",j);    
    }
    printf("\nThe Sum is : %d\n", sum);
    
    return 0;
    }
 ### 5. Write a C Program to print EVEN numbers from 1 to N using while loop.
 
     #include <stdio.h>
     int main()
     {
    int number;
   	//variable to store limit /N
   	int n;

	//assign initial value 
	//from where we want to print the numbers
	number=1;

	//input value of N
	printf("Enter the value of N: ");
	scanf("%d",&n);

	//print statement
	printf("Even Numbers from 1 to %d:\n",n);

	//while loop, that will print numbers 
	while(number<=n)
	{
		//Here is the condition to check EVEN number
		if(number%2==0)
			printf("%d ",number);
		
		// increasing loop counter by 1
		number++;
	}

	return 0;
}
### 6. Write a C Program to print ODD numbers from 1 to N using do while loop.

    #include <stdio.h>

    int main()
    {
	  //loop counter declaration
  	int number;
	  //variable to store limit /N
	  int n;

	//assign initial value 
	//from where we want to print the numbers
	number=1;

	//input value of N
	printf("Enter the value of N: ");
	scanf("%d",&n);

	//print statement
	printf("Odd Numbers from 1 to %d:\n",n);

	//while loop, that will print numbers 
	while(number<=n)
	{
		//Here is the condition to check ODD number
		if(number%2 != 0)
			printf("%d ",number);
		
		// increasing loop counter by 1
		number++;
	}

	return 0;
 }
 ### 7. Write a C Program to create a simple calculator using switch Statement.   
    #include<stdio.h>
    #include<conio.h>
    void main()
    {
    	int num1,num2,opt;
    	clrscr();
    	printf("Enter the first Integer:\n");
    	scanf("%d",&num1);
    	printf("Enter the second Integer:\n");
    	scanf("%d",&num2);
    	for(;;)
    	{
    		printf("\n\n\n\nEnter the your option:\n");
    		printf("1-Addition.\n2-Substraction.\n3-Multiplication.\n4-Division.\n5-Exit.\n");
    		scanf("%d",&opt);
    		switch(opt)
    		{
    			case 1:printf("\nAddition of  %d and %d is: %d",num1,num2,num1+num2);
    			break;
    			case 2:printf("\nSubstraction of %d  and %d is:  %d",num1,num2,num1-num2);
    			break;
    			case 3:printf("\nMultiplication of %d  and %d is:  %d",num1,num2,num1*num2);
    			break;  
    			case 4: 
    			if(num2==0)
    			{
    				printf("OOps Devide by zero\n");
    			}
    			else
    			{
    				printf("\n Division of %d  and %d is:  %d",num1,num2,num1/num2);
    			}  
    			break;
    			case 5: return 0;
    			break; 
    			default:printf("\n Enter correct option\n");
    			break; 
    		}
    	}
    	getch();
    }
 ### 8. Write a C Program to find the max between two numbers uding function.
   
      #include <stdio.h>
    /* Function declarations */
    int max(int num1, int num2);
    int min(int num1, int num2);
     int main() 
    {
    int num1, num2, maximum, minimum;
    
    /* Input two numbers from user */
    printf("Enter any two numbers: ");
    scanf("%d%d", &num1, &num2);
    
    maximum = max(num1, num2);  // Call maximum function
    minimum = min(num1, num2);  // Call minimum function
    
    printf("\nMaximum = %d\n", maximum);
    printf("Minimum = %d", minimum);
    
    return 0;
    }


   
     * Find maximum between two numbers.
 
     int max(int num1, int num2)
     {
      return (num1 > num2 ) ? num1 : num2;
      }


     * Find minimum between two numbers.
 
    int min(int num1, int num2) 
     {
    return (num1 > num2 ) ? num2 : num1;
     }
### 9.Write a program in C to check whether a number is a prime or not using the function

        #include <stdio.h>
    #include <conio.h>
    void main()
    {
    	int num,res=0;
    	clrscr();
    	printf("\nENTER A NUMBER: ");
    	scanf("%d",&num);
    	res=prime(num);
    	if(res==0)
    		printf("\n%d IS A PRIME NUMBER",num);
    	else
    		printf("\n%d IS NOT A PRIME NUMBER",num);
    	getch();
    }
    int prime(int n)
    {
    	int i;
    	for(i=2;i<=n/2;i++)
    	{
    		if(n%i!=0)
    			continue;
    		else
    			return 1;
    	}
    	return 0;
    }
  ### 10. Write a C Program for function (using call by value).
  #include <stdio.h>
 
 
void swap(int, int);
 
int main()
{
   int x, y;
 
   printf("Enter the value of x and y\n");
   scanf("%d%d",&x,&y);
 
   printf("Before Swapping\nx = %d\ny = %d\n", x, y);
 
   swap(x, y); 
 
   printf("After Swapping\nx = %d\ny = %d\n", x, y);
 
   return 0;
}
 
void swap(int a, int b)
{
   int temp;
 
   temp = b;
   b = a;
   a = temp;
    printf("Values of a and b is %d  %d\n",a,b);
}
### 11. Write a C Program for function (using call by reference).
    #include <stdio.h>
    void swap(int *n1, int *n2);
    int main()
    {
        int num1 = 5, num2 = 10;
        // address of num1 and num2 is passed
        swap( &num1, &num2);
        printf("num1 = %d\n", num1);
        printf("num2 = %d", num2);
        return 0;
    }
    void swap(int* n1, int* n2)
    {
        int temp;
        temp = *n1;
        *n1 = *n2;
        *n2 = temp;
    }
   ### 12. Write a C Program to take 5 values from the user and store them in an array. Print the elements stored in the array.
    #include <stdio.h>
    int main() {
    int values[5];
     printf("Enter 5 integers: ");
    // taking input and storing it in an array
    for(int i = 0; i < 5; ++i) {
     scanf("%d", &values[i]);
    }
    printf("Displaying integers: ");
    // printing elements of an array
    for(int i = 0; i < 5; ++i) {
     printf("%d\n", values[i]);
    }
    return 0;
    }
   ### 13. Write a C Program to find the average of n numbers using arrays.
        #include <stdio.h>
    int main()
    {
        int n, i;
        float num[100], sum = 0.0, average;
        printf("Enter the numbers of elements: ");
        scanf("%d", &n);
        while (n > 100 || n <= 0)
        {
            printf("Error! number should in range of (1 to 100).\n");
            printf("Enter the number again: ");
            scanf("%d", &n);
        }
        for(i = 0; i < n; ++i)
        {
            printf("%d. Enter number: ", i+1);
            scanf("%f", &num[i]);
            sum += num[i];
        }
        average = sum / n;
        printf("Average = %.2f", average);
        return 0;
    }  
   ### 14. Write a C Program to accept Sorted Array and do Search using Binary Search
     #include <stdio.h>

 

     void main()

   {

    int array[10];

    int i, j, num, temp, keynum;

    int low, mid, high; 

    printf("Enter the value of num \n");

    scanf("%d", &num);

    printf("Enter the elements one by one \n");

    for (i = 0; i < num; i++)

    {

        scanf("%d", &array[i]);

    }

    printf("Input array elements \n");

    for (i = 0; i < num; i++)

    {

        printf("%d\n", array[i]);

    }

    /*  Bubble sorting begins */

    for (i = 0; i < num; i++)

    {

        for (j = 0; j < (num - i - 1); j++)

        {

            if (array[j] > array[j + 1])

            {

                temp = array[j];

                array[j] = array[j + 1];

                array[j + 1] = temp;

            }

        }

    }

    printf("Sorted array is...\n");

    for (i = 0; i < num; i++)

    {

        printf("%d\n", array[i]);

    }

    printf("Enter the element to be searched \n");

    scanf("%d", &keynum);

    /*  Binary searching begins */

    low = 1;

    high = num;

    do

    {

        mid = (low + high) / 2;

        if (keynum < array[mid])

            high = mid - 1;

        else if (keynum > array[mid])

            low = mid + 1;

    } while (keynum != array[mid] && low <= high);

    if (keynum == array[mid])

    {

        printf("SEARCH SUCCESSFUL \n");

    }

    else

    {

        printf("SEARCH FAILED \n");

    }

    }
   ### 15. Write a C Program to Implement Linear Search
    #include <stdio.h>

 

    void main()

    {  int num;

 

    int i,  keynum, found = 0;

 

    printf("Enter the number of elements ");

    scanf("%d", &num);

    int array[num];

    printf("Enter the elements one by one \n");

    for (i = 0; i < num; i++)

    {

        scanf("%d", &array[i]);

    }

 

    printf("Enter the element to be searched ");

    scanf("%d", &keynum);

    /*  Linear search begins */

    for (i = 0; i < num ; i++)

    {

        if (keynum == array[i] )

        {

            found = 1;

            break;

        }

    }

    if (found == 1)

        printf("Element is present in the array at position %d",i+1);

    else

        printf("Element is not present in the array\n");

    }
  ###  16. Write a C Program to Sort N Numbers in Ascending Order using Bubble Sort.
     #include <stdio.h>

    #define MAXSIZE 10

 

    void main()

     {

    int array[MAXSIZE];

    int i, j, num, temp;

 

    printf("Enter the value of num \n");

    scanf("%d", &num);

    printf("Enter the elements one by one \n");

    for (i = 0; i < num; i++)

    {

        scanf("%d", &array[i]);

    }

    printf("Input array is \n");

    for (i = 0; i < num; i++)

    {

        printf("%d\n", array[i]);

    }

    /*   Bubble sorting begins */

    for (i = 0; i < num; i++)

    {

        for (j = 0; j < (num - i - 1); j++)

        {

            if (array[j] > array[j + 1])

            {

                temp = array[j];

                array[j] = array[j + 1];

                array[j + 1] = temp;

            }

        }

    }

    printf("Sorted array is...\n");

    for (i = 0; i < num; i++)

    {

        printf("%d\n", array[i]);

    }

    }
   ### 17. Write a C program to declare, assign and access a pointer variable
    #include <stdio.h>

    int main()
     {
    int num;    /*declaration of integer variable*/
    int *pNum;  /*declaration of integer pointer*/
 
    pNum=& num; /*assigning address of num*/
    num=100;    /*assigning 100 to variable num*/
 
    //access value and address using variable num
    printf("Using variable num:\n");
    printf("value of num: %d\naddress of num: %u\n",num,&num);
    //access value and address using pointer variable num
    printf("Using pointer variable:\n");
    printf("value of num: %d\naddress of num: %u\n",*pNum,pNum);
 
   return 0;
}
### 18. Write a C Program to Store Information of a Student Using Structure
    #include <stdio.h>
    struct student
    {
        char name[50];
        int roll;
        float marks;
    } s;
    int main()
    {
        printf("Enter information:\n");
        printf("Enter name: ");
        scanf("%s", s.name);
        printf("Enter roll number: ");
        scanf("%d", &s.roll);
        printf("Enter marks: ");
        scanf("%f", &s.marks);
        printf("Displaying Information:\n");
        printf("Name: ");
        puts(s.name);
        printf("Roll number: %d\n",s.roll);
        printf("Marks: %.1f\n", s.marks);
        return 0;
    }
   ### 19. Write a C Program to Find Factorial of a Number Using Recursion.   
    #include <stdio.h>
    long int multiplyNumbers(int n);
    int main()
    {
        int n;
        printf("Enter a positive integer: ");
        scanf("%d", &n);
        printf("Factorial of %d = %ld", n, multiplyNumbers(n));
        return 0;
    }
    long int multiplyNumbers(int n)
    {
        if (n >= 1)
            return n*multiplyNumbers(n-1);
        else
            return 1;
    }
   ### 20. Write a C Program to display Fibonacci Series using recursion
       #include<stdio.h>
     
    int Fibonacci(int);
     
    int main()
    {
       int n, i = 0, c;
     
       scanf("%d",&n);
     
       printf("Fibonacci series\n");
     
       for ( c = 1 ; c <= n ; c++ )
       {
          printf("%d\n", Fibonacci(i));
          i++; 
       }
     
       return 0;
    }
     
    int Fibonacci(int n)
    {
       if ( n == 0 )
          return 0;
       else if ( n == 1 )
          return 1;
       else
          return ( Fibonacci(n-1) + Fibonacci(n-2) );
    } 
