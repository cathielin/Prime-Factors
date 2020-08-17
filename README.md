# Prime-Factors
The program finds the prime factorization of a composite number using a multiset implemented from a binary tree. <br>
Written in C++11 in accordance to the Google C++ Style Guide <br>

NOTE: The code for this project has NOT been uploaded to GitHub publicly, as it was done for my data structures class. This was done to avoid future students from using my code as a violation of academic code conduct.

## Multiset Implementation 
The multiset was implemented from a binary tree. Duplicate keys in the tree can exist. 

### Multiset Testing 
Tests were ran with Google Test. A total of 18 tests were written to test 9 methods in the multiset. 
<ul>
  <li>Empty: Tests if the multiset is initially empty</li>
  <li>EmptyMultisetErrors, InvalidKeyErrors: Makes sure std::underflow_error is thrown
when the multiset is empty and std::out_of_range errors are thrown if the key is valid</li>
  <li>Removal, InsertionRemoval, MultipleInsertionRemoval, MultipleInsertionRemoval2: Tests a mix of
Insert() and Remove() functions being called, including testing that multiple occurences of a
key exist and can be removed one by one</li>
  <li>RemovalAll: Tests that the multiset is empty after all elements initially inserted are removed</li>
  <li> Floor, FloorRemove, Ceil, CeilRemoval, Min, MinRemoval, Max, MaxRemoval: Tests Floor(),
Ceil(), Min(), Max() respectively with and without removals from the multiset</li>
  
</ul>


## Prime Factors
The program is also able to provide the biggest and smallest prime factor, as well as the nearest prime factor smaller or greater than a given prime. <br>
The commands that the program can receive from the command line are listed below <br>
<ul> 
  <li><b>all</b>: prints all prime factors and the number of times they appear </li>
  <li><b>max</b>: prints largest prime factor for that number</li>
  <li><b>min</b>: prints smallest prime factor for that number</li>
  <li><b>near +prime</b>: prints the closest prime factor greater than the given prime number</li>
  <li><b>near -prime</b>: prints the closest prime factor smaller than the given prime number</li>
</ul>

## End Lessons / Notable Skills
Showcases ability to: 
<ul>
  <li>Write clean, well-documented industry standard-code that conforms to the Google C++ Style Guide</li>
  <li>Run unit tests using Google test </li>
  <li>Implement own data structures</li>
  <li>Print and handle errors when user gives incorrect commands</li>
</ul>
Demonstrates an understanding of:
<ul>
  <li>Data structures, particularly binary trees and multisets</li>
</ul>

## Example
$ ./prime_factors 4410 all </br>
2 (x1), 3 (x2), 5 (x1), 7 (x2), </br>
$ ./prime_factors 4410 min </br>
2 (x1) </br>
$ ./prime_factors 4410 max </br>
7 (x2) </br>
$ ./prime_factors 4410 near 5 </br>
5 (x1)
$ ./prime_factors 4410 near -5 </br>
3 (x2)
$ ./prime_factors 4410 near +5 </br>
7 (x2) </br>
$ ./prime_factors 4410 near +7 </br>
No match </br>
$ ./prime_factors 4410 test </br>
Command 'test' is invalid </br>
Possible commands are: all|min|max|near </br>
$ ./prime_factors 4410 near </br>
Command 'near' expects another argument: [+/-]prime </br>
