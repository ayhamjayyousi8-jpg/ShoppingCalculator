
using System;

namespace ShoppingCalculator
{
    class Program
    {
        static void Main(string[] sender)
        {
            double overallTotal = 0;
            bool keepAdding = true;

            while (keepAdding)
            {
                Console.Write("Enter price: ");
                double price = Convert.ToDouble(Console.ReadLine());

                Console.Write("Enter quantity: ");
                int quantity = Convert.ToInt32(Console.ReadLine());

                double productTotal = price * quantity;
                overallTotal += productTotal;

                Console.WriteLine($"Total = {productTotal}");

                Console.Write("Add another product? 1 = Yes, 0 = No: ");
                int choice = Convert.ToInt32(Console.ReadLine());

                if (choice == 0)
                {
                    keepAdding = false;
                }
                Console.WriteLine(); 
            }

            Console.WriteLine($"All Total = {overallTotal}");

            Console.WriteLine("\nPress any key to exit...");
            Console.ReadKey();
        }
    }
}









