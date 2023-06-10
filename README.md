# Interface

## Aim:
 To Develop a small bank application by declaring deposit() and withdrawal() as abstract methods in the interface. Get the choice from the user whether to perform withdrawal or deposit operation. After the operation completes, display the balance amount.

## Algorithm:
## Step 1:
Create an interface.

## Step 2:
Create a child class.

## Step 3:
Declare 2 functions deposit() and withdrawal() as abstract methods in the interface.

## Step 4:
Create those 2 functions in the child class and perform respective operation.

## Step 5:
Use while loop and and switch case to Get the choice from the user whether to perform withdrawal or deposit operation.

## Step 6:
After performing the functions display the remaining balance of the use

## Program:
```
Developed by: Suwetha.M
Register number: 21221230112

using System;

namespace ex09
{
    public interface bank
    {
        void deposit(int amt);
        void withdraw(int amt);
    }
    public class accnt : bank
    {
        public int balance = 50600, amt;
        int a = 1;
        public accnt()
        {

            while (a == 1)
            {
                Console.WriteLine("Enter 1 to deposit and 2 to withdraw and 3 to display your balance:");
                int choice = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine();
                switch (choice)
                {
                    case 1:
                        Console.WriteLine("Enter the amount to deposit");
                        amt = Convert.ToInt32(Console.ReadLine());
                        Console.WriteLine();
                        deposit(amt);
                        break;

                    case 2:
                        Console.WriteLine("Enter the amount to be withdrawn");
                        amt = Convert.ToInt32(Console.ReadLine());
                        Console.WriteLine();
                        withdraw(amt);
                        break;

                    case 3:
                        display();
                        break;
                }
            }
            Console.ReadKey();

        }
        public void deposit(int amt)
        {
            balance += amt;
        }
        public void withdraw(int amt)
        {
            balance -= amt;
        }
        public void display()
        {
            Console.WriteLine("Your remaining balance is " + balance);
            a = 0;
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            accnt p1 = new accnt();
        }
    }
}
```

## Output:

![244841047-fa45a4f0-623f-4e8e-b201-7c38b770f1a6](https://github.com/swemurali/Interface/assets/94165336/dd2fb9c5-63eb-488e-b8d2-010f15a0eba5)

## Result:
 C# program to develop a bank application using interface is implemented successfully.
