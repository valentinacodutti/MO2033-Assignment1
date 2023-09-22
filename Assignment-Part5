using System;

namespace GuessingGame
{
    class Program
    {
        static void Main(string[] args)
        {
            Game game = new Game();
            game.Start();
        }
    }

    class Game
    {
        private int target;
        private int attempts;

        public Game()
        {
            Random rand = new Random();
            this.target = rand.Next(1, 101);
            this.attempts = 0;
        }

        public void Start()
        {
            Console.WriteLine("Welcome to the Guessing Game! Try to guess the number between 1 and 100.");
            while (true)
            {
                Console.Write("Enter your guess: ");
                int guess = Convert.ToInt32(Console.ReadLine());
                this.attempts++;

                GuessResult result = CheckGuess(guess);
                if (result == GuessResult.Correct)
                {
                    Console.WriteLine($"Congratulations! You've guessed the number {this.target} in {this.attempts} attempts.");
                    break;
                }
                else if (result == GuessResult.TooHigh)
                {
                    Console.WriteLine("Your guess is too high. Try again!");
                }
                else
                {
                    Console.WriteLine("Your guess is too low. Try again!");
                }
            }
        }

        private GuessResult CheckGuess(int guess)
        {
            if (guess == this.target)
            {
                return GuessResult.Correct;
            }
            else if (guess > this.target)
            {
                return GuessResult.TooHigh;
            }
            else
            {
                return GuessResult.TooLow;
            }
        }
    }

    enum GuessResult
    {
        TooHigh,
        TooLow,
        Correct
    }
}
