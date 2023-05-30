# dzlast
//Задайте значение N. Напишите программу, которая выведет все натуральные числа в промежутке от N до 1. Выполнить с помощью рекурсии.
using System;

class Program
{
    static void Main(string[] args)
    {
        int n = 10;
        PrintNumbers(n);
    }

    static void PrintNumbers(int n)
    {
        if (n == 1)
        {
            Console.Write("1");
        }
        else
        {
            Console.Write($"{n}, ");
            PrintNumbers(n - 1);
        }
    }
}
//end
//Задайте значения M и N. Напишите программу, которая найдёт сумму натуральных элементов в промежутке от M до N.
using System;

class Program
{
    static void Main(string[] args)
    {
        int m = 5;
        int n = 10;
        int sum = SumNumbers(m, n);
        Console.WriteLine($"сумма чисел от {m} до {n} = {sum}");

        m = 8;
        n = 16;
        sum = SumNumbers(m, n);
        Console.WriteLine($"сумм чисел от {m} до {n} = {sum}");
    }

    static int SumNumbers(int m, int n)
    {
        if (m == n)
        {
            return m;
        }
        else
        {
            return m + SumNumbers(m + 1, n);
        }
    }
}
//end
