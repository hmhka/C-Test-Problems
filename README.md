C#-Test-Problems
===============

Programming problems on C#. Code rights reserved - http://www.c-sharpcorner.com/

--------------------------------------------------------------------------------
Problem 1

Write a program that converts 1 lower case letter ("a" - "z") to its corresponding 
upper case letter ("A" - "Z"). For example if the user enters "c" then the program 
will show "C" on the screen. 

Hint: You need to check the ASCII value in your program. 

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace VP_Assignment1
{
classProblem1
    {
staticvoid Main(string[] args)
        {
char a;
int b;
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
Console.WriteLine("Enter A Letter Between a-z:");
            a = Convert.ToChar(Console.ReadLine());
            b = (int)a;
if (b >= 97 && b <= 122)
            {
                b = b - 32;
 
                a = (char)b;
Console.WriteLine("In Upper Case Letter:" + a);
            }
else
            {
 
Console.WriteLine("You Enter Wrong Letter, Please Enter Letter Between a-z....!");
            }
Console.ReadKey();
 
 
        }
    }
}




-----------------------------------------------------------------------------------


Problem 2

Write a program that takes three points (x1, y1), (x2, y2) and (x3, y3) from the user
and the program will check wheteher or not all the three points fall on one straight line.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Programm2
{
classProblem2
    {
staticvoid Main(string[] args)
        {
int x1, x2, x3, y1, y2, y3;
int slope1, slope2, slope3;
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
Console.WriteLine("Enter the values of x1 and y1 coordinates of first point");
            x1 = Convert.ToInt32(Console.ReadLine());
            y1 = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Enter the values of x2 and y2 coordinates of second point");
            x2 = Convert.ToInt32(Console.ReadLine());
            y2 = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Enter the values of x3 and y3 coordinates of third point");
            x3 = Convert.ToInt32(Console.ReadLine());
            y3 = Convert.ToInt32(Console.ReadLine());
            slope1 = y2 - y1 / x2 - x1;
            slope2 = y3 - y1 / x3 - x1;
            slope3 = y3 - y2 / x3 - x2;
if (slope1 == slope2 && slope1 == slope3)
            {
 
Console.WriteLine("\nAll points are fall on one straight line ");
 
            }
else
            {
 
Console.WriteLine("\nAll points are not fall on one straight line");
            }
Console.ReadKey();
        }
    }
}

--------------------------------------------------------------------------------
Problem 3

Write a program that takes coordinates (x, y) of a center of a circle 
and its radius from the user, the program will determine whether a point 
lies inside the circle, on the circle or outside the circle.


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem3
{
classProblem3
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
int x, y,radius;
int radius_square, coordinates_calculation;
Console.WriteLine("Enter X coordinates of circle:");
            x = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Enter Y coordinates of circle:");
            y = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Enter Radius of circle:");
            radius = Convert.ToInt32(Console.ReadLine());
            radius_square = radius * radius;                      // Because equation of a circle is (x-a)^2+(y-b)^2=r^2
//And here at the origin (0,0) so we do here 
            coordinates_calculation = (x * x) + (y * y);
if (coordinates_calculation == radius_square)
            {
 
Console.WriteLine("Points Lies On The Circle");
            }
if (coordinates_calculation> radius_square )
            {
 
Console.WriteLine("Points Lies OutSide The Circle");
            }
if(coordinates_calculation <radius_square )
            {
 
Console.WriteLine("Points Lies InSide The Circle");
            }
Console.ReadKey();
 
        }
    }
}


--------------------------------------------------------------------------------
Problem 4

Write a program that takes a character from the user and determines whether 
the character entered is a capital letter, a small case letter, a digit or 
a special symbol. The following table shows the range of ASCII values for 
various characters.


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem4
{
classProblem4
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
char a;
int b;
Console.WriteLine("Enter A Charater:");
            a = Convert.ToChar(Console.ReadLine());
            b = (int)a;
if (b >= 65 && b <= 90)
            {
 
Console.WriteLine("Entered Character Is Capital Letter:");
            }
if (b >= 97 && b <= 122)
            {
 
Console.WriteLine("Entered Character Is Small Letter:");
            }
if (b >= 48 && b <= 57)
            {
 
Console.WriteLine("Entered Character Is  Digit:");
            }
if (b == 0 && b <= 47 || b >= 58 && b <= 64 || b >= 91 && b <= 96 || b >= 123 && b <= 127)
            {
 
Console.WriteLine("Entered Character Is Special Symbols:");
            }
Console.ReadKey();
        }
    }
}


--------------------------------------------------------------------------------
Problem 5

Write a program using a switch statement that takes one value from the user and asks about the type of conversion and then performs a conversion depending on the type of conversion. If user enters:

I -> convert from inches to centimeters. 
G -> convert from gallons to liters. 
M -> convert from mile to kilometer. 
P -> convert from pound to kilogram. 

If the user enters any other character then show a proper message.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem5
{
classProblem5
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
 
int value;
char choice;
double centimeter, liters, kilometer, kilogram;
Console.WriteLine("Enter A Digit Value:");
            value = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("\n\n Press Any Of The Given Choices \n I -> convert from inches to centimeters.\n G -> convert from gallons to liters.\n M -> convert from mile to 
kilometer.\n P -> convert from pound to kilogram.");
            choice = Convert.ToChar(Console.ReadLine());
 
switch (choice)
            {
 
case'I':
                    centimeter = value / 0.3937;                       //1 cm is equal is 0.3037 inch
Console.WriteLine("\n\nIn Centimeters:" + centimeter);
break;
case'i':
                    centimeter = value / 0.3937;
Console.WriteLine("\n\nIn Centimeters:" + centimeter);
break;
case'G':
                    liters = value * 3.78;                             // 1 gallon=3.78 litters
Console.WriteLine("\n\nIn Litters:" + liters);
break;
case'g':
                    liters = value * 3.78;                             // 1 gallon=3.78 litters
Console.WriteLine("\n\nIn Litters:" + liters);
break;
case'M':
                    kilometer = value * 1.60;
Console.WriteLine("\n\nIn kilometers:" + kilometer);
break;
case'm':
                    kilometer = value * 1.60;
Console.WriteLine("\n\nIn kilometers:" + kilometer);
break;
case'P':
                    kilogram = value * 0.453;
Console.WriteLine("\n\nIn KiloGrams:" + kilogram);
break;
case'p':
                    kilogram = value * 0.453;
Console.WriteLine("\n\nIn KiloGrams:" + kilogram);
break;
 
default:
Console.WriteLine("You Enter A Invalid Choice, Please Enter A Valid Choice...!");
break;
 
            }
Console.ReadKey();
        }
    }
}


--------------------------------------------------------------------------------
Problem 6

In a company, worker efficiency is determined on the basis of the time required for a worker to complete a specific job. If the time taken by the worker is between 2 - 3 hours, then the worker is said to be highly efficient. If the time required by the worker is 3 - 4 hours, then the worker is ordered to increase their speed. If the time taken is 4 - 5 hours then the worker is given training to improve his speed and if the time taken by the worker is more than 5 hours then the worker must leave the company. If the time taken by the worker is input through the keyboard then find the efficiency of the worker.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem6
{
classProblem6
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
int time;
Console.WriteLine("Enter Time Required For A Worker To Complete A Particular Job In Hours");
            time = Convert.ToInt32(Console.ReadLine());
if (time >= 2 && time >=3)
            {
 
Console.WriteLine("Worker Efficiency Is Highly Efficient.");
            }
if (time >= 3 && time >=4)
            {
 
Console.WriteLine("Worker Should Improve His Speed.");
            }
if (time >= 4 && time >= 5)
            {
 
Console.WriteLine("Worker Is Given Training To Improve His Speed.");
 
            }
if (time > 5)
            {
 
Console.WriteLine("Worker Should Leave The Company.");
            }
Console.ReadKey();
        }
    }
}

--------------------------------------------------------------------------------
Problem 7

Write a program using conditional operators to determine whether a year entered through the keyboard is a leap year or not.


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem7
{
classProblem7
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
int year;
string a;
Console.WriteLine("Enter A Year:");
            year = Convert.ToInt32(Console.ReadLine());
           a= year % 4 == 0 ? "Year Is Leap": "It Is Not A Leap Year:";
Console.WriteLine(a);
Console.ReadKey();
        }
    }
}




--------------------------------------------------------------------------------
Problem 8

Write a program using a switch statement that takes one character value from the user and checks whether the entered value is an arithmetic operator, logical operator, conditional operator, relational operator or something else.


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem8
{
classProblem8
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
string value;
 
Console.WriteLine("Enter A Operator:");
            value = Console.ReadLine();
 
switch (value)
            {
 
case"+":
Console.WriteLine("This Is Arithmatic Operator:");
break;
case"-":
Console.WriteLine("This Is Arithmatic Operator:");
break;
case"*":
Console.WriteLine("This Is Arithmatic Operator:");
break;
case"%":
Console.WriteLine("This Is Arithmatic Operator:");
break;
case"/":
Console.WriteLine("This Is Arithmatic Operator:");
break;
case"&":
Console.WriteLine("This Is Arithmatic Operator:");
break;
case"--":
Console.WriteLine("This Is Arithmatic Operator:");
break;
case"++":
Console.WriteLine("This Is Arithmatic Operator:");
break;
case"|":
Console.WriteLine("This Is Logical Operator:");
break;
case"!":
Console.WriteLine("This Is Logical Operator:");
break;
case"^":
Console.WriteLine("This Is Logical Operator:");
break;
case"&&":
Console.WriteLine("This Is Logical Operator:");
break;
case"||":
Console.WriteLine("This Is Logical Operator:");
break;
 
case"==":
Console.WriteLine("This Is Relational Operator:");
break;
case"!=":
Console.WriteLine("This Is Logical Operator:");
break;
case"<":
Console.WriteLine("This Is Logical Operator:");
break;
case">":
Console.WriteLine("This Is Logical Operator:");
break;
case"<=":
Console.WriteLine("This Is Logical Operator:");
break;
case">=":
Console.WriteLine("This Is Logical Operator:");
break;
case"?":
Console.WriteLine("This Is Conditional Operator:");
break;
default:
Console.WriteLine("This Is Something Else Operator:");
break;
            }
Console.ReadKey();
        }
    }
}



--------------------------------------------------------------------------------
Problem 9

Write a program that prints an identity matrix using a for loop, in other words takes a value n from the user and shows the identity table of size n * n.


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem9
{
classProblem9
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
int size;
Console.WriteLine("Enter The Size Of The Identity Matrix:");
            size = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("\n\n Identity Matrix\n\n");
for (int i = 0; i < size; i++)
            {
 
for (int j = 0; j < size; j++)
                {
 
if (i == j)
                    {
 
Console.Write(1);
                    }
else
                    {
Console.Write(0);
                    }
 
                }
Console.WriteLine("\n");
            }
Console.ReadKey();
        }
    }
}




--------------------------------------------------------------------------------
Problem 10

Write a program using a for loop that prints the following series. 

1 2 4 8 16 21 64 128 …nth iteration.


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem10
{
classProblem10
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
int value;
double result;
Console.WriteLine("Enter Some Value:");
            value = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("\nSeries Is:\n");
for (int i = 0; i <= value; i++)
            {
                result = Math.Pow(2, i);
Console.Write(result);
Console.Write(" ");
            }
Console.ReadKey();
        }
    }
}



--------------------------------------------------------------------------------
Problem 11

Write a program using a for loop that prints the following output (you need to find a pattern to print letters in this order):

A B D H P

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem11
{
classProblem11
    {
staticvoid Main(string[] args)
        {
char ch;
int i = 1;
int j = 0;
 
while(i<=16)
            {
 
                j = i + 64;
             ch = (char)j;
Console.Write(ch);
Console.Write(" ");
             i = i * 2;
            }
Console.ReadKey();
        }
    }
}


--------------------------------------------------------------------------------
Problem 12

Write a program using a loop that prints the following output. 

1 2 2 3 3 3 4 4 4 4 5 5 5 5 5 6 6 6 6 6 6 . . . nth iteration.


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem12
{
classProblem12
    {
staticvoid Main(string[] args)
        {
int value;
Console.WriteLine("Enter A Value:");
            value = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("\n");
 
for (int i = 1; i <= value; i++)
            {
 
for (int j = 1; j <= i; j++)
                {
 
Console.Write(i);
                }
Console.Write(" ");
            }
Console.ReadKey();
        }
    }
}


--------------------------------------------------------------------------------
Problem 13

Write a program to print all the ASCII values and their equivalent characters using a while loop. The ASCII values vary from 0 to 255.


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem13
{
classProblem13
    {
staticvoid Main(string[] args)
        {
 
char ch;
 
int i = 0;
while(i<=255)
            {
 
Console.Write(i);
Console.Write(" ");
            ch = (char)i;
Console.WriteLine(ch);
            i++;
            }
Console.ReadKey();
        }
    }
}


--------------------------------------------------------------------------------
Problem 14

Write a program to print all the ASCII values and their equivalent characters using a do-while loop. The ASCII values vary from 10 to 255.


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem15
{
classProblem15
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
char ch;
 
int i = 10;
do
            {
 
Console.Write(i);
Console.Write(" ");
                ch = (char)i;
Console.WriteLine(ch);
                i++;
            } while (i <= 255);
Console.ReadKey();
        }
    }
}



--------------------------------------------------------------------------------
Problem 16

Write a program that takes one value from the user and checks whether the entered value is a character, integer or special symbol.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem16
{
classProblem16
    {
staticvoid Main(string[] args)
        {
char a;
int b;
Console.WriteLine("Enter A Value:");
            a = Convert.ToChar(Console.ReadLine());
            b = (int)a;
if (b >= 65 && b <= 90)
            {
                a = (char)b;
 
Console.WriteLine("Entered Value Is Character:" +a);
            }
if (b >= 97 && b <= 122)
            {
 
Console.WriteLine("Entered Value Is Character:"+a);
            }
if (b >= 48 && b <= 57)
            {
 
Console.WriteLine("Entered Value Is  Integer:"+a);
            }
if (b == 0 && b <= 47 || b >= 58 && b <= 64 || b >= 91 && b <= 96 || b >= 123 && b <= 127)
            {
 
Console.WriteLine("Entered Value Is Special Symbols:");
            }
Console.ReadKey();
        }
    }
}


--------------------------------------------------------------------------------
Problem 17

Write a program that takes an integer as an input from the user and prints if it is a prime or composite number.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem17
{
classProblem17
    {
staticvoid Main(string[] args)
        {
int num;
int i = 2;
Console.WriteLine("Enter A Number:");
            num = Convert.ToInt32(Console.ReadLine());
while ( i < num)
            {
 
if (num % i == 0)
                {
Console.WriteLine("Entered Number Is  A Composite  Number.");
 
break;
 
                }
                i++;
            }
if (i == num)
            {
Console.WriteLine("Entered Number Is  A Prime Number.");
            }
if (num==0||num==1)
            {
Console.WriteLine("Entered Number Is Not A Composite  Number Nor A Prime Number.");
            }
Console.ReadKey();
 
        }
    }
}

--------------------------------------------------------------------------------
Problem 18

Write a program that prints the Fibonacci series using a loop. 

1 1 2 3 5 8 13 21 34 …

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem18
{
classProblem18
    {
staticvoid Main(string[] args)
        {
int num;
int  next;
int first=0;
int second=1;
 
Console.WriteLine("Enter The Number Of Terms Of Fibonacci Series You Want:");
            num = Convert.ToInt32(Console.ReadLine());
for (int i = 0; i < num; i++)
            {
 
if (i <= 1)
                {
                    next = i;
 
                }
else
                {
                    next = first + second;
                    first = second;
                    second = next;
                }
Console.Write(next);
Console.Write(" ");
            }
Console.ReadKey();
        }
    }
}


--------------------------------------------------------------------------------
Write a program using a for loop that prints the following output on the screen. 

* 
** 
*** 
**** 
*** 
** 
*


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem19
{
classProblem19
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
for (int i = 0; i < 4; i++)
            {
 
for (int j = 0; j <= i; j++)
                {
 
Console.Write("*");
 
                }
Console.WriteLine("\n");
            }
for (int i = 0; i <= 2; i++)
            {
 
for (int j = 3; j >i; j--)
                {
 
Console.Write("*");
 
                }
Console.WriteLine("\n");
            }
Console.ReadKey();
        }
    }
}

--------------------------------------------------------------------------------
Write a program using a for loop that prints the following output on the screen. 

* 
*** 
***** 
******* 
********* 
***********
 

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem20
{
classProblem20
    {
staticvoid Main(string[] args)
        {
int num;
int k = 0;
Console.WriteLine("Enter The Value To Draw A Rectangle Shape:");
            num = Convert.ToInt32(Console.ReadLine());
for (int i = 0; i < num; i++)
            {
for (int j = 0; j <= k;j++)
                {
Console.Write("*");
                }
Console.WriteLine("\n");
                k += 2;
            }
Console.ReadKey();
        }
    }
}


--------------------------------------------------------------------------------
Problem 21

Write a program to print all Armstrong numbers between 1 and 500. If the sum of the cubes of each digit of the number is equal to the number itself, then the number is called an Armstrong number. For example, 153 = (1 * 1 * 1) + (5 * 5 * 5) + (3 * 3 * 3).
 

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem21
{
classProblem21
    {
staticvoid Main(string[] args)
        {
int FirstDigit, SecondDigit, LastDigit,num;
Console.WriteLine("All Armstrong Numbers Between 1 And 500.\n");
for (int i = 1; i <= 500; i++)
            {
                num = i;
                LastDigit = num % 10;
                num = num / 10;
                SecondDigit = num % 10;
                num = num / 10;
                FirstDigit = num % 10;
if ((FirstDigit * FirstDigit * FirstDigit) + (SecondDigit * SecondDigit * SecondDigit) + (LastDigit * LastDigit * LastDigit) == i)
                {
Console.WriteLine("This Is A Armstrong Number:" + i);
                }
 
 
            }
Console.ReadKey();
        }
    }
}

--------------------------------------------------------------------------------
Problem 22

Write a program using a for loop that prints the following output on the screen. 

$$$$$$$$$$$ 
$ $ 
$ $ 
$ $ 
$$$$$$$$$$

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem22
{
classProblem22
    {
staticvoid Main(string[] args)
        {
int check1=1;
int check2=2;
int check3=3;
for (int a = 1; a <= 11; a++)
            {
Console.Write("$");
            }
Console.WriteLine("\n");
for (int b = 1; b <= 3; b++)
            {
for (int c = 1; c <= 1; c++)
                {
Console.Write("$");
                }
if (b == check1)
                {
for (int d = 1; d <= 9; d++)
                    {
Console.Write(" ");
                    }
                }
if (b == check2)
                {
for (int d = 1; d <= 8; d++)
                    {
Console.Write(" ");
                    }
                }
if (b == check3)
                {
for (int d = 1; d <= 8; d++)
                    {
Console.Write(" ");
                    }
                }
 
Console.Write("$"); 
Console.WriteLine("\n");
            }
for (int e = 1; e <= 10; e++)
            {
Console.Write("$");
            }
Console.ReadKey();
        }
    }
}

--------------------------------------------------------------------------------
Problem 23

Write a program using a loop that takes one value n from the user and shows the factorial of all prime numbers that are less then n, for example if n = 10 then the program will print the factorial of 2, 3, 5 and 7.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem23
{
classProblem23
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
int j;
int num;
int fact=1;
Console.WriteLine("Enter The Number:");
            num = Convert.ToInt32(Console.ReadLine());
 
for (int i = 1; i <= num; i++)
            {
 
for (j = 2; j <i; j++)
                {
 
 
 
if (i % j == 0)
                        {
 
 
goto outloop;
 
                        }
 
                }
                outloop:
if (j == i)
                    {
                        fact = 1;
for(int k=1;k<=i;k++)
                        {
                        fact=fact*k;
                        }
Console.WriteLine("Factorial Of "+i+" Prime Number Is "+fact);
                    }
//if (i == 0 || i == 1)
//{
//    Console.WriteLine("Entered Number Is Not A Composite  Number Nor A Prime Number.");
//}
              }
Console.ReadKey();
            }
        }
 
}

--------------------------------------------------------------------------------
Problem 24

Write a program to display the sum of the following series using a loop.

1*x + 2*x2 + 3*x3 + 4*x4 + 5*x5 + … + n*xn

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem24
{
classProblem24
    {
staticvoid Main(string[] args)
        {
int num;
double sum=0;
double x;
Console.WriteLine("Enter The Range Value To Display The Sum Like This Series \n1*^x + 2*x^2 + 3*x^3 + 4*x^4 + 5*x^5 + … + n*x^n");
            num = Convert.ToInt32(Console.ReadLine());
for (int i = 1; i <= num; i++)
            {
                x = (double)i;
 
                sum = sum +(i * Math.Pow(x,x));
            }
Console.WriteLine("\nThe Sum Is :" + sum);
Console.ReadKey();
        }
    }
}

--------------------------------------------------------------------------------
Problem 25

Write a program to display the sum of the following series, in other words the sum of the factorial of the odd series.

1! + 3! + 5! + 7! + 9! + . . . + n!
 

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem25
{
classProblem25
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
int num; 
int fact1=1;
int sum=0;
Console.WriteLine("Enter Number To Display The Sum Of The Following Series i.e. sum of the factorial of odd series\n Like This 1! + 3! + 5! + 7! + 9! + . . . + n!");
            num = Convert.ToInt32(Console.ReadLine());
for (int i = 1; i <= num; i++)
            {
 
if (i % 2 != 0)
                {
                    fact1 = 1;
for (int j = 1; j <= i; j++)
                    {
                        fact1 = fact1 * j;
 
                    }
 
                    sum = sum + fact1;
                }
 
            }
Console.WriteLine("\nThe Sum Of The Following Series: " + sum);
Console.ReadKey();
        }
    }
}

--------------------------------------------------------------------------------
Problem 26

Write a program to display the sum of the following series. 

2/1! + 4/3! + 6/5! + 8/7! + 10/9! + . . . + n/(n-1)

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem26
{
classProblem26
    {
staticvoid Main(string[] args)
        {
int num;
double fact1 = 1;
double temp;
double sum = 0;
Console.WriteLine("Enter Number To Display The Sum Of The Following Series i.e. sum of the factorial of series\n Like This 2/1! + 4/3! + 6/5! + 8/7! + 10/9! + . . . +
n/(n-1)!");
            num = Convert.ToInt32(Console.ReadLine());
for (int i = 1; i <= num; i++)
            {
 
if (i % 2 != 0)
                {
                    fact1 = 1;
for (int j = 1; j <= i; j++)
                    {
                        fact1 = fact1 * j;
 
                    }
 
                }
if (i % 2 == 0)
                {
                    temp = i / fact1;
 
 
                    sum = sum + temp;
                }
 
 
            }
Console.WriteLine("\nThe Sum Of The Following Series: " + sum);
Console.ReadKey();
        }
    }
}

--------------------------------------------------------------------------------
Problem 27

Write a program to display the sum of the following series, in other words the sum of the factorial of the odd series multiplied by x where the power of x is the square of the corresponding number. 

X1*1! + X9*3! + X25*5! + X49*7! + X81*9! + . . . + Xn2*n!

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem27
{
classProblem27
    {
staticvoid Main(string[] args)
        {
int num;
int fact1 = 1;
int sum = 0;
 
int x;
int temp;
Console.WriteLine("Enter Number To Display The Sum Of The Following Series i.e.sum of the factorial of odd series multiply with x \n where power of x is square of corresponding number.\nX1*1! + X9*3! + X25*5! + X49*7! + X81*9! + . . . + Xn2*n!");
            num = Convert.ToInt32(Console.ReadLine());
for (int i = 1; i <= num; i++)
            {
                fact1 = 1;
if (i % 2 != 0)
                {
for (int j = 1; j <= i; j++)
                    {
                        fact1 = fact1 * j;
 
                    }
 
                        x =i*i;
                        temp = x * fact1;
 
                        sum = sum + temp;
 
                }
 
 
            }
Console.WriteLine("\nThe Sum Of The Following Series: " + sum);
Console.ReadKey();
        }
    }
}

--------------------------------------------------------------------------------
Problem 28

Write a program that displays the following output on the screen. 

1 2 3 4 5 
1 4 9 16 25 
1 8 27 64 125

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem28
{
classProblem28
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
int temp1;
int temp2;
for (int i = 1; i <= 5; i++)
            {
 
Console.Write(i);
Console.Write(" ");
            }
Console.WriteLine("\n");
for (int i = 1; i <= 5; i++)
            {
                temp1 = i * i;
 
Console.Write(temp1);
Console.Write(" ");
            }
Console.WriteLine("\n");
for (int i = 1; i <= 5; i++)
            {
                temp2 = i * i*i;
 
Console.Write(temp2);
Console.Write(" ");
            }
 
Console.ReadKey();
        }
    }
}

--------------------------------------------------------------------------------
Problem 29

Write a program that displays the following output on the screen. 

####$#### 
###$#$### 
##$###$## 
#$#####$# 
$#######$

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem29
{
classProblem29
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
int firstdollar = 8;
int seconddollar;
int k;
int x = 8;
int space = 0; int val;
int j;
int i = 1;
while (i <= 5)
            {
                j = 4;
                val = x;
                seconddollar = val;
while (j <= val)                            //This loop is for left side triangle
                {
if (j == firstdollar)
                    {
Console.Write("$");
                    }
else
Console.Write("#");
                    j++;
                }
if (i == 1)
                    val--;
                k = 1;
while (k <= space)                          //This loop is for center triangle
                {
Console.Write("#");
                    k++;
                }
 
                space = 2 * i - 1;
while (val >= 4)                            //This loop is for right side triangle
                {
if (val == seconddollar)
                    {
Console.Write("$");
                    }
else
                    {
Console.Write("#");
                    }
 
                    val--;
 
                }
                i++;
                x--;
                firstdollar--;
Console.WriteLine();
 
 
            }
Console.ReadKey();
        }
    }
}
--------------------------------------------------------------------------------
Write a program to produce the following output:

A B C D E F G F E D C B A 
A B C D E F *F E D C B A 
A B C D E *** E D C B A 
A B C D ***** D C B A 
A B C ******** C B A 
A B ********** B A 
A ************ A

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem30
{
classProblem30
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
int i = 1;
int x = 71;
int space = 0;
int j;
int k;
int val;
char ch;
char ch1;
while (i <= 7)
            {
                j=65;
                val = x;
while (j <= val)
                {                                            //This loop is for left side triangle
 
                    ch = (char)j;
Console.Write(ch);
                    j++;
                }
if (i == 1)
                    val--;
                k = 1;
while (k <= space)
                {                                            //This loop is for center side triangle
Console.Write("*");
                    k++;
                }
 
                space = 2 * i - 1;
while (val >= 65)                            //This loop is for Right side triangle
                {
                    ch1 = (char)val;
Console.Write(ch1);
                    val--;
 
                }
                i++;
                x--;
Console.WriteLine();
 
            }
Console.ReadKey();
        }
    }
}
--------------------------------------------------------------------------------
Problem 31

Write a program to produce the following output: 

1 
2 3 
4 5 6 
7 8 9 10

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem31
{
classProblem31
    {
staticvoid Main(string[] args)
        {
int space=30;
int num = 1;
for (int i = 1; i < 5;i++ )
            {
for (int j = 1; j <= space; j++)
                {
Console.Write(" ");
                }
                space = space - 2;
for (int k = 1; k <= i; k++)
                {
Console.Write(num);
Console.Write("  ");
                    num++;
                }
Console.WriteLine("\n");
            }
Console.ReadKey();
        }
    }
}
--------------------------------------------------------------------------------
Problem 32

Write a program that takes 10 values from the user in an array and then shows the number of prime values in the array.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem32
{
    classProblem32
{
    staticvoid Main(string[] args)
{
    int[] array = newint[10];
    int count=0;
    int i;
    int j;
    int k=2;
    for ( i = 0; i < 10; i++)
            {
    Console.WriteLine("Enter " +i+" Value");
    array[i] = Convert.ToInt32(Console.ReadLine());
}
for ( j = 0; j < 10; j++)
            { 
for( k=2;j<array[count];k++)
                {
if (array[count] % k == 0)
                       {
goto to; 
                      }
                }
            to:
if (k == array[count])
                {
Console.WriteLine("Entered Number Is " +array[count]+ "  A Prime Number.");
                }
if (array[count] == 0 || array[count] == 1)
                {
Console.WriteLine("Entered Number Is " +array[count]+" Not A Composite  Number Nor A Prime Number.");
                }
                count++;
            }
Console.ReadKey();
        }
    }
}

--------------------------------------------------------------------------------
Problem 33

How many printf statements will be executed by this program and rewrite the following program without using a goto statement.

void main( ) 
{ 
int i, j, k ; 
for ( i = 1 ; i <= 3 ; i++ ) 
{ 
for ( j = 1 ; j <= 3 ; j++ ) 
{ 
for ( k = 1 ; k <= 3 ; k++ ) 
{ 
if ( i == 3 && j == 3 && k == 3 ) 
goto out ; 
else 
printf ( "%d %d %d\n", i, j, k ) ; 
} 
} 
} 
out : 
printf ( "Out of the loop at last!" ) ; 
}
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem33
{
classProblem33
    {
staticvoid Main(string[] args)
        {
int i, j, k ;
for ( i = 1 ; i <= 3 ; i++ )
            {
for ( j = 1 ; j <= 3 ; j++ )
                {
for ( k = 1 ; k <= 3 ; k++ )
                    {
if (i == 3 && j == 3 && k == 3)
                        {
break;// without goto.
                        }
 
else
                        {
Console.WriteLine("I " + i + "J " + j + "K " + k);
 
                        }
                    }
                }
            }
Console.WriteLine("In This Program WritLine Will Print 26 Times.");
Console.ReadKey();
 
        }
    }
}
--------------------------------------------------------------------------------
Write a program that takes n values from user and then sorts them in ascending order.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem34
{
classProblem34
    {
staticvoid Main(string[] args)
        {
int num;
int temp;
 
 
Console.WriteLine("Enter The Numbers You Want To Enter:");
            num = Convert.ToInt32(Console.ReadLine());
int[] array = newint[num];
 
for (int i = 0; i < num; i++)
            {
 
Console.WriteLine("Enter " + i + " Value:");
                array[i] = Convert.ToInt32(Console.ReadLine());
            }
for (int i = 0; i < num ; i++)
            {
for (int j = 0; j < num - 1; j++)
                {
 
if (array[j] > array[j + 1])
                    {
                        temp = array[j];
                        array[j] = array[j + 1];
                        array[j + 1] = temp;
                    }
                }
            }
Console.WriteLine("In Ascending Order:");
for (int i = 0; i < num; i++)
            {
 
Console.WriteLine(array[i]);
            }
Console.ReadKey();
        }
    }
}
--------------------------------------------------------------------------------
Write a program that takes n values from the user and then sorts them using a Bubble sort.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem35
{
classProblem35
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\tUOG\n");
int num;
int temp;
 
 
Console.WriteLine("Enter The Numbers You Want To Enter:");
            num = Convert.ToInt32(Console.ReadLine());
int[] array = newint[num];
 
for (int i = 0; i < num; i++)
            {
 
Console.WriteLine("Enter " + i + " Value:");
                array[i] = Convert.ToInt32(Console.ReadLine());
            }
for (int i = 0; i < num ; i++)
            {
for (int j = 0; j < num-1;j++ )
                {
 
if (array[j] > array[j+1])
                    {
                        temp = array[j];
                        array[j] = array[j + 1];
                        array[j + 1] = temp;
                    }
                }
            }
Console.WriteLine("\nIn Ascending Order Using Bubble Sort:");
for (int i = 0; i < num; i++)
            {
 
Console.WriteLine(array[i]);
            }
Console.ReadKey();
        }
    }
}

--------------------------------------------------------------------------------
Problem 36

Write a program that takes n values in an array and then search for a value in the array using a binary search algorithm. Hint: You need to sort that array first because a binary search can be applied only on a sorted array.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem36
{
classProblem36
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
int num;
int temp;
int first = 0;
int last;
int mid;
int found;
int count = 1;
 
 
Console.WriteLine("Enter The Numbers You Want To Enter:");
            num = Convert.ToInt32(Console.ReadLine());
int[] array = newint[num];
 
for (int i = 0; i < num; i++)
            {
 
Console.WriteLine("Enter " + count+ " Value:");
                array[i] = Convert.ToInt32(Console.ReadLine());
                count++;
            }
for (int i = 0; i < num; i++)
            {
for (int j = 0; j < num - 1; j++)
                {
 
if (array[j] > array[j + 1])
                    {
                        temp = array[j];
                        array[j] = array[j + 1];
                        array[j + 1] = temp;
                    }
                }
            }
Console.WriteLine("Enter The Number You Want To Search:");
            found = Convert.ToInt32(Console.ReadLine());
 
            last = num - 1;
            mid = (first + last) / 2;
 
while (first <= last)
            {
if (array[mid] < found)
                    first = mid + 1;
elseif (array[mid] == found)
                {
Console.WriteLine( found + " Found At Location " +mid);
break;
                }
else
                    last = mid - 1;
 
                mid = (first + last) / 2;
            }
if (first > last)
Console.WriteLine("Not Found "+found+ " Is Not Present In The List.\n");
Console.ReadKey();
        }
    }
}
--------------------------------------------------------------------------------
Problem 37

Write a program that copies the values of one array to a second array in reverse order.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem37
{
classProblem37
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
int[] array1 = newint[] { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
int[] array2 = newint[10];
Console.WriteLine("Array1 Values:");
for (int i = 0; i < 10; i++)
            {
 
Console.Write(array1[i]);
Console.Write(" ");
            }
int j=9;
Console.WriteLine("\n\nCopied Values To The Array2 In Reverse Order:");
for (int i = 0; i < 10; i++)
            { 
            array2[i]=array1[j];
            j--;
            }
for (int i = 0; i < 10; i++)
            {
Console.Write(array2[i]);
Console.Write(" ");
            }
Console.ReadKey();
        }
    }
}
--------------------------------------------------------------------------------
Problem 38

Create two arrays, student_rollno and student_marks, both of the same size. The first array will save the rollnos of students and the second array will save the marks of students against his rollno. For example if student_rollno[0] contains 197 then student_marks[0] will contain the marks of roll no 197.

You need to print the roll number of the student with maximum marks.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem38
{
classProblem38
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
int[] student_rollno = newint[5];
int[] student_marks = newint[5];
int max;
int count = 0;
int temp = 1;
 
 
for (int i = 0; i < 5; i++)
            {
 
Console.WriteLine("Enter The " + temp + " Students Roll No:");
                student_rollno[i] = Convert.ToInt32(Console.ReadLine());
 
Console.WriteLine("Enter The " + temp + " Students Marks:");
                student_marks[i] = Convert.ToInt32(Console.ReadLine());
                temp++;
            }
//for (int i = 0; i < 5; i++)
//{
//    Console.WriteLine(student_rollno[i]);
//}
            max = student_marks[0];
 
for (int i = 0; i < 5; i++)
            {
if (max < student_marks[i])
                {
                    count++;
                    max = student_marks[i];
 
                }
 
            }
Console.WriteLine("\n");
if (count == 0)
            {
Console.WriteLine("Student Roll No= "+student_rollno[0]+" Students Maximum Marks Is= "+max);
            }
if (count == 1)
            {
Console.WriteLine("Student Roll No= " + student_rollno[1] + " Students Maximum Marks Is= " + max);
            }
if (count == 2)
            {
Console.WriteLine("Student Roll No= " + student_rollno[2] + " Students Maximum Marks Is= " + max);
            }
if (count == 3)
            {
Console.WriteLine("Student Roll No= " + student_rollno[3] + " Students Maximum Marks Is= " + max);
            }
if (count == 4)
            {
Console.WriteLine("Student Roll No= " + student_rollno[4] + " Students Maximum Marks Is= " + max);
            }
Console.ReadKey();
        }
    }
}

--------------------------------------------------------------------------------
Problem 39

Write a function that takes one value as a parameter and display the sum of the digits in the value. For example, if the user has passed 125 then the function will print 1+2+5 = 7.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem39
{
classProblem39
    {
 
staticvoid Main(string[] args)
        {
Problem39 p = newProblem39();
string num;
int a;
int count;
Console.WriteLine("Enter A Number:");
            num=Console.ReadLine();
            count = num.Length;
            a = int.Parse(num);
            p.cal(a,count);
Console.ReadKey();
        }
privatevoid cal(int num,int count)
        {
int a;
int sum = 0;
 
for (int i = 1; i <= count; i++)
            {
                a = num % 10;
                num = num / 10;
                sum = sum + a;
            }
Console.WriteLine("The Sum Of The Individual Numbers Of The Entered Number Is:" + sum);
        }
    }
}
--------------------------------------------------------------------------------
Problem 40

Write a function that takes two values, n1 and n2, as arguments and multiply the n1 by itself n2 times. In other words, calculate n1n2 and then return the result to the main function that will display the result.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem40
{
classProblem40
    {
 
staticvoid Main(string[] args)
        {
Problem40 p = newProblem40();
double n1, n2;
Console.WriteLine("Enter n1 Value:");
            n1 = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Enter n2 Value:");
            n2 = Convert.ToInt32(Console.ReadLine());
Console.WriteLine( "The n1^n2 Is  :" +p.Cal(n1, n2));
Console.ReadKey();
        }
 
privatedouble Cal(double n1, double n2)
        { 
            n1 = Math.Pow(n1, n2);
 
return n1;
        }
    }
}
--------------------------------------------------------------------------------
Problem 41

Write a program that will input a charater "a" value from the user. You need to use a switch statement to decide if the value of a is "t" then you need to call the table function. If the value of a is "f" then call the factorial function, if the value of a is "p" then call the prime function, if the value of a is "s" then call the search function.

You need to write four functions in your program as in the following:

Table(int n1,n2) 
Factorial(int n3) 
Prime(int n4) 
Search(char n5[], char c, char choice) 
Table function will print the table of n1 from 1 to n2. 
Factorial function will print the factorial of n3 if n3 is a multiple of 2. 
Prime function will print the n4 if n4 is prime. 
Search function will take the first argument n5 as an array of characters and the second element a character to be searched for in the array and the third element a character to decide which searching algorithm is to be used, in other words if the user has passed the value of c as "s" then the Search function will perform the sequential search but if the value of c is something else then the Search function will perform a binary search. 
The structure of your program will be like this. You need to make it exactly working.

Switch(a) 
{ 
case ‘f’: 
factorial(); 
break; 
case ‘p’: 
prime(); 
break; 
case ‘t’: 
table(); 
break; 
case ‘s’: 
search(); 
break; 
}
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem41
{
classProblem41
    {
staticvoid Main(string[] args)
        {
Problem41 p1 = newProblem41();
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\tUOG\n");
System.Console.Write(" Press t For Table   \n Press   f For Factorial  \n Press  p For Prime\n Press  s For Search\n Press Character(except t,f,p) For Sequential Search");
System.Console.Write("\n\nInput a Character Value: ");
string a = System.Console.ReadLine();
 
switch (a)
            {
case"t":
                    System.Console.Write("Enter Number: ");
int n1 = Convert.ToInt32(System.Console.ReadLine());
                    System.Console.Write("Enter Number: ");
int n2 = Convert.ToInt32(System.Console.ReadLine());
                    p1.table(n1, n2);
break;
case"f":
                    System.Console.Write("Enter number: ");
int n3 = Convert.ToInt32(System.Console.ReadLine());
                    p1.factorial(n3);
break;
case"p":
                    System.Console.Write("Enter Nmber To Check It is Prime Or Not: ");
int n4 = Convert.ToInt32(System.Console.ReadLine());
                    p1.prime(n4);
break;
case"s":
int num;
char temp;
int count = 1;
char found;
Console.WriteLine("Enter The Numbers You Want To Enter:");
                    num = Convert.ToInt32(Console.ReadLine());
char[] array = newchar[num];
 
for (int i = 0; i < num; i++)
                    {
 
Console.WriteLine("Enter " + count + " Character:");
                        array[i] = Convert.ToChar(Console.ReadLine());
                        count++;
                    }
for (int i = 0; i < num; i++)
                    {
for (int j = 0; j < num - 1; j++)
                        {
 
if (array[j] > array[j + 1])
                            {
                                temp = array[j];
                                array[j] = array[j + 1];
                                array[j + 1] = temp;
                            }
                        }
                    }
Console.WriteLine("Enter The Character You Want To Search:");
                    found = Convert.ToChar(Console.ReadLine());
                    p1.Binary_search(array, found, a, num);                  // Binary Seacrh Function call
break;
default:
Console.WriteLine("Sequential Search");
int num1;
char temp1;
int count1 = 1;
char found1;
Console.WriteLine("Enter The Numbers You Want To Enter:");
                    num1 = Convert.ToInt32(Console.ReadLine());
 
char[] array1 = newchar[num1];
for (int i = 0; i < num1; i++)
                    {
 
Console.WriteLine("Enter " + count1 + " Character:");
                        array1[i] = Convert.ToChar(Console.ReadLine());
                        count1++;
                    }
for (int i = 0; i < num1; i++)
                    {
for (int j = 0; j < num1 - 1; j++)
                        {
 
if (array1[j] > array1[j + 1])
                            {
                                temp1 = array1[j];
                                array1[j] = array1[j + 1];
                                array1[j + 1] = temp1;
                            }
                        }
                    }
Console.WriteLine("Enter The Character You Want To Search:");
                    found1 = Convert.ToChar(Console.ReadLine());
                    p1.Binary_search(array1, found1, a, num1);                  // Binary Seacrh Function call
//  System.Console.WriteLine("Invalid choice");
break;
            }
Console.ReadKey();
        }
//starts table funtion
privatevoid table(int n1, int n2)
        {
int i;
int result;
            System.Console.WriteLine("Table Of " + n1 + " Is");
for (i = 1; i <= n2; i++)
            {
                result = n1 * i;
                System.Console.WriteLine(n1 + "X" + i + "=" + result);
            }
 
        }
 
//starts factorial function
privatevoid factorial(int n3)
        {
int fact = 1, i;
 
if (n3 % 2 == 0)
            {
for (i = 1; i <= n3; i++)
                { fact = fact * i; }
                System.Console.Write("Factorial Is: " + fact);
 
            }
else
            {
                System.Console.Write("Enter number Is Not A Multple Of 2, So Cannot See Its Factorial");
            }
        }
 
//starts prime function
privatevoid prime(int n4)
        {
int c;
for (c = 2; c <= n4 - 1; c++)
            {
if (n4 % c == 0)
                {
                    System.Console.Write("Not A Prime Number");
break;
                }
            }
if (c == n4)
                System.Console.Write("Enter Number is Prime number");
        }
 
//starts search function
privatevoid Binary_search(char[] array, char found, string s, int num)
        {
 
if (s == "s")
            {
 
int first = 0;
int last;
int mid;
last = num - 1;
mid = (first + last) / 2;
while (first <= last)
                {
if (array[mid] < found)
first = mid + 1;
elseif (array[mid] == found)
                    {
Console.WriteLine(found + " Found At Location " + mid);
break;
                    }
else
last = mid - 1;
mid = (first + last) / 2;
                }
if (first > last)
Console.WriteLine("Not Found " + found + " Is Not Present In The List.\n");
Console.ReadKey();
            }
else {
int b=1;
int i;
bool flag = true;
for ( i = 0; i < num; i++)
                {
if (array[i] == found)
                    {
 
Console.WriteLine(found + " Found At Location " + b);
                        flag = false;
                    }
                    b++;
 
                }
if(flag)
                {
Console.WriteLine(found + "Is Not In The List ");
                }
            }
        }
        }
  
  
--------------------------------------------------------------------------------
Problem 42

Write two functions, max(int,int) and prime(int). The max function will take two arguments and will return the maximum of the two numbers to main. Then main function will pass this calculated factorial to the prime function that will show whether that passed value is prime or not.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem42
{
classProblem42
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
Problem42 p = newProblem42();
int num1, num2;
int picker;
Console.WriteLine("Enter The num1:");
            num1 = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Enter The num2:");
            num2 = Convert.ToInt32(Console.ReadLine());
           picker= p.max(num1, num2);
Console.WriteLine("The Maximum Is " +picker);
 
            p.prime(picker);
Console.ReadKey();
 
        }
 
privateint max(int num1,int num2)
        {
if (num1 > num2)
            {
return num1;
            }
else
            {
return num2;
            }
 
        }
privatevoid prime(int num)
        {
int i = 2;
while (i < num)
            {
 
if (num % i == 0)
                {
Console.WriteLine("\nThis Number Is  A Composite  Number.");
 
break;
 
                }
                i++;
            }
if (i == num)
            {
Console.WriteLine("\nThis Number Is  A Prime Number.");
            }
if (num == 0 || num == 1)
            {
Console.WriteLine("\nThis Number Is Not A Composite  Number Nor A Prime Number.");
            }
 
        }
    }
}

--------------------------------------------------------------------------------

Problem 43

Write a function that takes four arrays of the same size as arguments; array1, array2, array3 and array4. The function will multiply the corresponding values of array1 and array2 and will save the result at the same index as array3, in other words array3[0] = array1[0] * array2[0] and so on. Then create another function and pass all four arrays to that function as an argument where you need to compare array1, array2 and array3 and save the max value in array4. In other words if array1[0] = 10, array2[0] = 5, array3[0]= 11 then you need to save the max value, in other words array4[0] = 11. In the main function, show all the values of array4.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem43
{
classProblem43
    {
 
publicstaticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
Problem43 p = newProblem43();
int[] array1 = newint[] { 1, 3, 5, 7, 9 };
int[] array2 = newint[] { 2, 4, 6, 8, 10 };
int[] array3 = newint[5];
int[] array4 = newint[5];
int[] temp = newint[5];
int[] temp2 = newint[5];
          temp=  p.mullarray(array1, array2, array3, array4);
Console.WriteLine("Values Of  Array3 Which Is The Result Of Multiplication Of The Corresponding Indexes Of The Array1 And Array2:");
for (int i = 0; i < 5; i++)
          {
Console.WriteLine(temp[i]);
          }
         temp2= p.mullarray(array1, array2, temp, array4);
 
Console.WriteLine("\nMaximum Values Of The All Of Them Which Stored In The Array4:");
for (int i = 0; i < 5; i++)
         {
Console.WriteLine(temp2[i]);
         }
Console.ReadKey();
 
        }
publicint[] mullarray(int[] a1,int[] a2,int[] a3,int[] a4)
      {
for (int i = 0; i < 5; i++)
          {
              a3[i] = a1[i] * a2[i];
          }
 
return a3;
      }
publicint[] maxarray(int[] a1,int[] a2,int[] a3,int[] a4)
      {
for (int i = 0; i < 5; i++)
          {
 
if (a1[i] > a2[i]&&a1[i]>a3[i])
              {
                  a4[i] = a1[i];
              }
if (a2[i] > a1[i] && a2[i] > a3[i])
              {
                  a4[i] = a2[i];
              }
if (a3[i] > a1[i] && a3[i] > a2[i])
              {
                  a4[i] = a3[i];
              }
 
          }
return a4;
 
 
      }
    }
}

--------------------------------------------------------------------------------

Problem 44

If the lengths of the sides of a triangle are denoted by a, b, and c, then the area of the triangle is given by:

Area = Sïƒ–S(S-a)(S-b)(S-c) 
where, S = ( a + b + c ) / 2

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem44
{
classProblem44
    {
staticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
double a, b, c, S;
double Area;
Console.WriteLine("Enter Side A");
            a = Convert.ToDouble(Console.ReadLine());
Console.WriteLine("Enter Side B");
            b = Convert.ToDouble(Console.ReadLine());
Console.WriteLine("Enter Side C");
            c = Convert.ToDouble(Console.ReadLine());
 
            S = (a + b + c) / 2;
            Area = S* Math.Sqrt(S * (S - a) * (S - b) * (S - c));
Console.WriteLine("Area Of The Triangle Is: " + Area);
Console.ReadKey();
 
        }
    }
}

--------------------------------------------------------------------------------

OOP Section

Problem 45

Create a class of student that stores characteristcs of a student, like studentID, studentName, studentDOB, studentRollNo, studentEmail, studentGPA of the last 5 semesters and other related information of the student. (You may set some properties Boolean and some readonly.)

Calculate the CGPA of each student using the function calculateCGPA(…).
The student with the highest CGPA will be considerd CR of the class. There should be a function that will compare the CGPA of students and will declare a student having a greater CGPA as CR.
The program should be able to take input of 5 students from the user; definitely there will be a function that will take input from the user.
You need to use a Setter for setting the values of the data members of the class and a Getter function for getting the values of the data members of the class. (You can use a property as an alternative.)
The default value for each student's GPA should be 3.0. (You need to use an array for storing GPAs of the last 5 semesters. You may simply initialize the array with 3.0 in the constructor).
All data members should be private.
Member functions can be public.
The program must be able to add two objects, in other words if we add two students then all their corresponding data members will be added one by one. (Operator Overloading).
The program must contain an explicitly defined copy constructor.
StudentID and StudentGPA of the last 5 semesters must be constant or readonly.
The value of studentGPA of the last 5 semesters must be selected from a enum that may contain values {1.0, 2.0, 3.0, and 4.0}.
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace Problem45
{
classStudent
    {
privateint studentID;
privatestring studentName;
privatestring studentDOB;
privatestring studentEmail;
privateint studentRollNo;
privatedouble studentGPA;
 
enumgpa_Range
        {
           one=1,two=2,three=3,four=4
        };
 
gpa_Range g;
publicstaticvoid Main(string[] args)
        {
Console.WriteLine("\t\tName: Ehtesham Mehmood\n\t\tRoll No: 11014119-131\n\t\tSection: AE\n \t\t        UOG\n");
Student s1 = newStudent();
Student s2 = newStudent();
Student s3 = newStudent();
Student s4 = newStudent();
Student s5 = newStudent();
Student s6 = newStudent();
Student comp = newStudent();
double[] picker = newdouble[5];
double[] st = newdouble[5];
Console.WriteLine("..............Data Of Student s1..............");
            picker=s1.inputUser();
            st[0]=s1.calculateCGPA(picker);
Console.WriteLine("..............Data Of Student s2..............");
            picker = s2.inputUser();
            st[1] = s2.calculateCGPA(picker);
            s6 = s1 + s2;
            s6.Display();
Console.WriteLine("..............Data Of Student s3..............");
            picker = s3.inputUser();
            st[2] = s3.calculateCGPA(picker);
Console.WriteLine("..............Data Of Student s4..............");
            picker = s4.inputUser();
            st[3] = s4.calculateCGPA(picker);
Console.WriteLine("..............Data Of Student s5..............");
            picker = s5.inputUser();
            st[4] = s5.calculateCGPA(picker);
Console.WriteLine("..............Here CR Selection Is Perform..............");
            comp.compareCGPA(st[0], st[1], st[2], st[3], st[4]);
 
Console.ReadKey();
 
        }
public Student()
        {
            studentGPA = 3.0;
        }
public Student(Student s)                            // copy constructor
        {
 
            studentID = s.studentID;
            studentName = s.studentName;
            studentDOB = s.studentDOB;
            studentEmail = s.studentEmail;
            studentRollNo = s.studentRollNo;
            studentGPA = s.studentGPA;
        }
publicdouble[] arr = newdouble[5];
publicdouble[] inputUser()
        {
 
Console.WriteLine("Enter Student ID:");
            studentID=Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Enter Student Name:");
            studentName = Console.ReadLine();
Console.WriteLine("Enter Student DOB:");
            studentDOB = Console.ReadLine();
Console.WriteLine("Enter Student Email:");
            studentEmail = Console.ReadLine();
Console.WriteLine("Enter Student Roll No:");
            studentRollNo = Convert.ToInt32(Console.ReadLine());
int choice; int count=1;
for (int i = 0; i < 5; i++)
            {
Console.WriteLine("Enter Student GPA Semester: "+ count);
Console.WriteLine("Press 1 For 1gpa\nPress 2 For 2gpa\nPress 3 For 3gpa\nPress 4 For 3gpa");
                choice = Convert.ToInt32(Console.ReadLine());
 
                g = (gpa_Range)choice;
 
switch (g)
                { 
 
casegpa_Range.one:
 
                        arr[i] = (double)gpa_Range.one;
break;
casegpa_Range.two:
 
                        arr[i] = (double)gpa_Range.two;
break;
casegpa_Range.three:
 
                        arr[i] = (double)gpa_Range.three;
break;
casegpa_Range.four:
 
                        arr[i] = (int)gpa_Range.four;
break;
 
 
                }
                count++;
            }
 
 
return arr;
        }
publicdouble calculateCGPA(double[] pick)
        {
double cgpa = 0;
for (int i = 0; i < 5; i++)
            {
                cgpa = cgpa +pick[i];
            }
            cgpa = cgpa / 5;
            studentGPA = cgpa;
return cgpa;
        }
publicvoid compareCGPA(double s1,double s2,double s3, double s4, double s5)
        { 
if((s1>s2) && (s1>s3)&&(s1>s4)&&(s1>s5))
               {
Console.WriteLine("Student s1 Is Become The CR With CGPA Of " + s1);
 
               }
if ((s2 > s1) && (s2 > s3) && (s2 > s4) &&( s2 > s5))
              {
Console.WriteLine("Student s1 Is Become The CR With CGPA Of " + s2);
 
              }
if ((s3 > s1) && (s3 > s2) && (s3 > s4) &&( s3 > s5))
              {
Console.WriteLine("Student s2 Is Become The CR With CGPA Of " + s3);
 
              }
if ((s4 > s1) &&( s4 > s2) &&( s4 > s3) && (s4 > s5))
              {
Console.WriteLine("Student s1 Is Become The CR With CGPA Of " + s4);
 
              }
if ((s5 > s1) && (s4 > s2) &&( s5 > s3) && (s5 > s4))
              {
Console.WriteLine("Student s1 Is Become The CR With CGPA Of " + s5);
 
              }
        }
publicstaticStudentoperator +(Student ss1, Student ss2)
        {
 
Student result = newStudent();
            result.studentName = string.Copy(ss1.studentName);
string.Concat(result.studentName, ss2.studentName);
            result.studentDOB = string.Copy(ss1.studentDOB);
string.Concat(result.studentDOB, ss2.studentDOB);
            result.studentEmail = string.Concat(ss1.studentEmail, ss2.studentEmail);
            result.studentID = ss1.studentID + ss2.studentID;
            result.studentRollNo = ss1.studentRollNo + ss2.studentRollNo;
            result.studentGPA = ss1.studentGPA + ss2.studentGPA;
 
return result;
 
        }
publicvoid Display()
        {
Console.WriteLine("Student ID IS " + studentID);
Console.WriteLine("Student Name IS " + studentName);
Console.WriteLine("Student DOB IS " + studentDOB);
Console.WriteLine("Student Email IS " + studentEmail);
Console.WriteLine("Student Roll No IS " + studentRollNo);
Console.WriteLine("Student CGPS IS " + studentGPA);
 
        }
    }
}

--------------------------------------------------------------------------------

--------------------------------------------------------------------------------
