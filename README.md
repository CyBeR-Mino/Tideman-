
---

# Tideman Voting System

## Overview

This program implements the Tideman voting system, also known as the ranked pairs method. This voting system selects a single winner from a set of candidates based on ranked preferences submitted by voters. This implementation is part of the CS50 course assignment and demonstrates advanced election algorithms.

## Features

- Preference Recording: Records voter preferences to determine how many voters prefer one candidate over another.
- Pair Addition: Identifies and records pairs of candidates where one is preferred over the other.
- Pair Sorting: Sorts pairs in descending order by the margin of victory.
- Cycle Detection: Ensures that locking pairs does not create cycles in the candidate graph.
- Winner Determination: Determines and prints the winner of the election based on the locked pairs graph.

## Usage

1. Compile the Program:

  
   gcc -o tideman tideman.c -lcs50
   
2. Run the Program:

  
   ./tideman [candidate ...]
   
   Replace [candidate ...] with the names of the candidates. For example:

  
   ./tideman Alice Bob Charlie
   
3. Input Voting Data:

   After running the program, you will be prompted to enter the number of voters and their preferences for each candidate. 

## Example

Suppose there are three candidates: Alice, Bob, and Charlie. To run the program with these candidates:

./tideman Alice Bob Charlie
You will then be asked for the number of voters and their rankings. For example:

Number of voters: 3
Rank 1: Alice
Rank 2: Bob
Rank 3: Charlie
...
The program will output the winner of the election based on the ranked pairs method.

## Code Explanation

- Preference Recording:
  - The record_preferences function updates the preference matrix based on voter input.

- Pair Addition:
  - The add_pairs function identifies pairs of candidates where one is preferred over the other and records the strength of the preference.

- Pair Sorting:
  - The sort_pairs function sorts the pairs in descending order by the strength of victory.

- Cycle Detection:
  - The cycle_detector function checks for cycles in the graph to prevent locking pairs that would create a cycle.

- Winner Determination:
  - The print_winner function identifies and prints the candidate with no incoming edges in the locked pairs graph.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Author

[Ye Yint Aung]

---
