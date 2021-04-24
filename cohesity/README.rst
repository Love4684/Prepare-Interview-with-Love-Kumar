
.. contents::
   :local:
   :depth: 2
   

Q.1
===============================================================================

.. image:: https://github.com/Love4684/Prepare-Interview-with-Love-Kumar/blob/main/cohesity/6.png

list
------------

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;

      int main()
       {     
           list<int> list1;
           list<int> list2;
           int n, temp;
           cin >> n;
           for (int i = 0; i < n; ++i)
           {
              cin >> temp;
              list1.push_back(temp);
           }
            for (int i = 0; i < n; ++i)
           {
              cin >> temp;
              list2.push_back(temp);
           }
           list1.merge(list2);
           list1.sort();
           list1.unique();

           for (auto it : list1)
           {
               cout << it << " ";
           }

           return 0;
      }

input

.. code:: c++

      5
      4 2 7 1 5
      3 4 8 1 6

output

.. code:: c++

      1 2 3 4 5 6 7 8 


Q.2
===============================================================================

.. image:: https://github.com/Love4684/Prepare-Interview-with-Love-Kumar/blob/main/bytedance/S.E/2.png

cpp code
------------

.. code:: c++

    // A DP based CPP
    // program to print
    // first nth Tribinacci
    // numbers.
    #include <bits/stdc++.h>
    using namespace std;

    string printTrib(string x)
    {int n = stoi(x);
        int dp[n+1];
        dp[0] = dp[1] = 0;
        dp[2] = 1;

        for (int i = 3; i <= n; i++)
            dp[i] = dp[i - 1] +
                    dp[i - 2] +
                    dp[i - 3];

        return to_string(dp[n]);
    }

    // Driver code
    int main()
    {
        string n = "5";
        cout<<printTrib(n);
        return 0;
    }
