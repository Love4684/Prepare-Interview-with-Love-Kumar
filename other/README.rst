
.. contents::
   :local:
   :depth: 2
   
S.E
===============================================================================

Q.1 solution
----------

.. image:: https://github.com/Love4684/Prepare-Interview-with-Love-Kumar/blob/main/other/1.png

.. image:: https://github.com/Love4684/Prepare-Interview-with-Love-Kumar/blob/main/other/2.png

.. image:: https://github.com/Love4684/Prepare-Interview-with-Love-Kumar/blob/main/other/3.png

.. image:: https://github.com/Love4684/Prepare-Interview-with-Love-Kumar/blob/main/other/4.png

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;
      int main()
      {string str;
         cin >> str;
         map<char, int> m ;
         for (int i = 0; i < str.size(); ++i)
         {
            m[str[i]]++;
         }
         int count = 2*(min(m['u'], m['d']) + min(m['r'], m['l']));
         cout << count;
      }
      
      
Q.2 solution
----------

.. image:: https://github.com/Love4684/Prepare-Interview-with-Love-Kumar/blob/main/other/5.png

.. image:: https://github.com/Love4684/Prepare-Interview-with-Love-Kumar/blob/main/other/6.png

.. image:: https://github.com/Love4684/Prepare-Interview-with-Love-Kumar/blob/main/other/7.png

.. image:: https://github.com/Love4684/Prepare-Interview-with-Love-Kumar/blob/main/other/8.png

.. image:: https://github.com/Love4684/Prepare-Interview-with-Love-Kumar/blob/main/other/9.png



Q 3. string transformation
===============================================================================

.. code:: c++

      Prepbuddy is a notorious kid so to teach him a lesson his teacher gave him homework and wrote two strings of the same length on the blackboard and asks prepbuddy to make         them equal using operations of only one type: take two adjacent characters of one of the strings and invert them both. Inversion transforms 0 to 1 and 1 to 0To make the         problem even harder, Prepbuddy must use a minimal number of inversion operations.

      Help Prepbuddy to complete his difficult homework. And also the strings are binary means contain only 0's and 1's.

      For example, if the two strings were "0101" and "1111" one way to make them equal is to invert two characters in the middle of the first string to get "0011" and "1111"         and then invert two first characters of the second string to get "0011" and "0011". Note that there are other ways to complete the task with two operations in this               example.

      Input format
      The first line contains the number of test cases T.
      The first line of each test case contains N, the length of the strings.
      The second and the third lines contain the strings themselves.
      The sum of values of n for all test cases in one input data doesn't exceed 10^5.

      Output format
      For each test case print one line the minimal required number of inversion operations to make the strings equal, or  −1 if it is impossible to make the strings equal.

      Constraints
      1≤T≤100
      1≤N≤10^5

      Time Limit
      2 second

      Example
      Input
      2
      4
      0101
      1111
      3
      011
      111

      Output
      2
      -1

Q.3 solution
----------
