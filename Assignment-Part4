using System;

namespace MO2033_Assignment1
{
    class Calculator
    {
        static void Main(string[] args)
        {
            GreetUser("John");  // Test the greeting method with different names.
            GreetUser("Alice");

            Console.WriteLine("Welcome to the Calculator!");

            while (true)
            {
                Console.WriteLine("\nSelect operation:\n1. Add\n2. Subtract\n3. Multiply\n4. Divide\n5. Exit");
                int choice = Convert.ToInt32(Console.ReadLine());

                if (choice == 5)
                {
                    Console.WriteLine("Thank you for using the Calculator. Goodbye!");
                    break;
                }

                Console.Write("Enter first number: ");
                double num1 = Convert.ToDouble(Console.ReadLine());

                Console.Write("Enter second number: ");
                double num2 = Convert.ToDouble(Console.ReadLine());

                switch (choice)
                {
                    case 1:
                        Console.WriteLine($"Result: {Add(num1, num2)}");
                        break;
                    case 2:
                        Console.WriteLine($"Result: {Subtract(num1, num2)}");
                        break;
                    case 3:
                        Console.WriteLine($"Result: {Multiply(num1, num2)}");
                        break;
                    case 4:
                        try
                        {
                            Console.WriteLine($"Result: {Divide(num1, num2)}");
                        }
                        catch (DivideByZeroException)
                        {
                            Console.WriteLine("Error: Division by zero is not allowed.");
                        }
                        break;
                    default:
                        Console.WriteLine("Invalid choice.");
                        break;
                }
            }
        }

        static void GreetUser(string name)
        {
            Console.WriteLine($"Hello, {name}!");
        }

        static double Add(double a, double b)
        {
            return a + b;
        }

        static double Subtract(double a, double b)
        {
            return a - b;
        }

        static double Multiply(double a, double b)
        {
            return a * b;
        }

        static double Divide(double a, double b)
        {
            if (b == 0) throw new DivideByZeroException();
            return a / b;
        }
    }
}
