# BubbleSort
My Bubble Sort Algorithm 

Hello, I created a bubble sort algorithm for my computer science work. Its not perfect but it works. I am open to opinions or improvements on how to make it more efficient or easier to understand. Thank you.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Bubblesort
{
    class Program
    {
        static void Main(string[] args)
        {
            int tempStore;
            int arraySize;

            // Creating an integer array with 9 elements
            int[] numlist = new int[9] { 9, 8, 7, 6, 5, 10, 56, 4, 1};

            // Finding how many elements are in the array
            arraySize = numlist.Length;

            // Iteratre through the array
            for(int x = 0; x < arraySize; x++)
            {
                // Iterate throught the array
                for (int i = 0; i < arraySize - 1; i++)
                {
                    // Check is previous element is greater than the preceding element
                    if (numlist[i] > numlist[i + 1])
                    {
                        // Tempory store the 1st element in temp
                        tempStore = numlist[i];
                        // re-asign preceding element to first element
                        numlist[i] = numlist[i + 1];
                        // re-asign 2nd element to tempstore
                        numlist[i + 1] = tempStore;
                    }
                    else
                    {
                        // continue with loop
                        continue;
                    }

                }

                // Loop back through the array to check again.
            }

            // Loop through each element in array
            for (int j = 0; j < arraySize; j++)
            {
                // Print elements in the array
                Console.Write(numlist[j] + " ");
            }

            Console.ReadLine();

        }
    }
}

