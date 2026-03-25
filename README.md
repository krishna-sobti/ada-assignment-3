Krishna Sobti
btech cyber security 4th sem
2401410034

Fractional Knapsack Algorithm in C++
This repository contains a C++ implementation of the Fractional Knapsack problem, a classic algorithmic challenge solved using the Greedy approach. Unlike the 0/1 Knapsack problem, this version allows you to take fractions of an item to maximize the total value in a knapsack of a specific capacity.

Logic Overview

The algorithm follows a simple two-step greedy strategy:

Ratio Calculation & Sorting: It calculates the value-to-weight ratio for each item. Items are then sorted in descending order based on this ratio to prioritize those with the highest "bang for your buck".
+1

Greedy Selection:

If the knapsack can carry the entire weight of the current item, the item is added fully.

If the remaining capacity W is less than the item's weight, the algorithm takes a fraction of the item to fill the remaining space exactly and then stops.

Code Components

struct Item: A data structure used to store the value and weight of each item.

cmp function: A custom comparator that helps the sort function arrange items by their value/weight ratio.

fractionalKnapsack: The core function that processes the items and calculates the maximum total value possible.
+1

Implementation Details

Parameter	Description
W	
The maximum weight capacity of the knapsack.

Item arr[]	
An array of items, each containing a value and weight.

totalValue	
A double precision variable to store the accumulated value.
+1

Note: The current example in the code uses a knapsack capacity of 50 units with items valued at 60, 100, and 120.

How to Run

Ensure you have a C++ compiler installed (like g++).

Save the code to a file named knapsack.cpp.

Compile and run using:

Bash
g++ knapsack.cpp -o knapsack
./knapsack



Job Sequencing with Deadlines (C++)
📖 Overview
This project implements the Job Sequencing with Deadlines problem using a greedy algorithm in C++.
The goal is to maximize total profit by scheduling jobs within their deadlines. Each job takes 1 unit of time, and only one job can be scheduled at a time.
🚀 Features
Sorts jobs based on maximum profit
Efficiently schedules jobs within deadlines
Calculates:
Total number of jobs completed
Maximum profit earned
Optimal job sequence
🧠 Algorithm Used
Greedy Approach
Sort all jobs in descending order of profit
Find the maximum deadline
Create a time slot array
Assign each job to the latest available slot before its deadline
Compute total profit and job count
📂 Code Structure
🔹 struct Job
Represents a job with:
id → Job ID
deadline → Last time slot to complete job
profit → Profit earned
🔹 compare()
Custom comparator to sort jobs by profit (descending).
🔹 jobSequencing()
Main function that:
Sorts jobs
Allocates time slots
Assigns jobs optimally
Prints results
🔹 main()
Initializes job list
Calls the sequencing function
🧾 Example Input
Job arr[] = {
    {1, 2, 100},
    {2, 1, 19},
    {3, 2, 27},
    {4, 1, 25},
    {5, 3, 15}
};
📊 Example Output
Number of jobs done: 3
Total profit: 142
Job sequence: J1 J3 J5
⚙️ How to Run
🖥️ Compile
g++ job_sequencing.cpp -o job
▶️ Execute
./job
⏱️ Time & Space Complexity
Type	Complexity
Time	O(n²)
Space	O(n)
📌 Applications
Task scheduling
CPU job scheduling
Project management optimization
Resource allocation problems


