using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace NumberGuessingGame
{   
    class Program
    {
        static void Main(string[] args) 
        {   
            Random r = new Random();

            int winNum = r.Next(0, 100);

            bool win = false;


            do
            {
                Console.WriteLine("Guess a number in between 0 and 100: ");
                string s = Console.ReadLine();

                Console.WriteLine(winNum);
                Console.WriteLine("-------");

                int i = int.Parse(s);

                if (i > winNum) 
                {
                    Console.WriteLine("Too high! Guess lower ...");

                }
                else if (i <winNum) 
                {
                    Console.WriteLine("Too low! Guess higher...: ");
                }
                else if (i == winNum) 
                {
                    Console.WriteLine("You win!");
                    win=true;
                }
                Console.WriteLine();    
            } while (win==false);
            Console.WriteLine("Thank you for playing the game!") ;
            Console.Write("Press any key to finish. ");
            Console.ReadKey(true);
        
        }   
    }
}