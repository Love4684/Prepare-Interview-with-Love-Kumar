
.. contents::
   :local:
   :depth: 3

Infosys Interview Questions
===============================================================================

product of all prime number less than given number
===============================================================================

.. code:: c++

    #include<bits/stdc++.h>
    using namespace std;

    int main()
     {      
         int n, result = 1, j;
            cin >> n;
            for(int i = 2; i < n; i++ )
            {
                for (j = 2; j < i; j++)
                {
                    if(i%j == 0)
                    {
                        break;
                    }
                }
                if(i == j)
                    result *= i;
            }
            cout << result << endl;
        return 0;
    }
    // ans = 30


Program to print the diamond shape
===============================================================================

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;

      int main()
       {      
           int n, j, k;
              cin >> n;
              for(int i = 1; i <= n; i++ )
              {
                  for (j = n; j > i; j--)
                  {
                      cout << " ";
                  }
                  for (k = 1; k <= i; k++)
                  {
                      cout << "* ";
                  }
                  cout << endl;
              }
              for(int i = 1; i < n; i++ )
              {
                  for (j = 1; j <= i; j++)
                  {
                      cout << " ";
                  }
                  for (k = n-1; k >= i; k--)
                  {
                      cout << "* ";
                  }
                  cout << endl;
              }

          return 0;
      }

output

.. code:: c++

          * 
         * * 
        * * * 
       * * * * 
      * * * * * 
       * * * * 
        * * * 
         * * 
          * 

Find kth Largest element in array
===============================================================================

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;

            int main()
             {     
                 vector<int> v = {2, 4, 6, 3, 5};
                 int  k = 2; 

                priority_queue<int, vector<int>, greater<int> > minheap;
                for (int i = 0; i < 5; ++i)
                 {
                     minheap.push(v[i]);
                     if(minheap.size() > k)
                     {
                        minheap.pop();
                     }
                 }
                 cout << minheap.top() << " ";     
                return 0;
            }

.. code:: c++

      5

find the nth Prime Number
===============================================================================

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;

      int main()
       {     
           int j, n = 5, count = 0;
           for (int i = 2; i > 0; ++i)
           {  int  flag = 0;
               for ( j = 2; j < i; ++j)
               {
                   if(i%j == 0)
                   {
                      flag = 1;
                      break;
                   }
               }
               if(i == j)
               {
                  count++;
               }
               if(count == n)
               {
                  cout << i;
                  break;
               }
           }
           return 0;
      }


Longest Increasing Subsequence
===============================================================================

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;

      int main()
       {     
           vector<int> v = {3, 5, 9, 7, 8};
           vector<int> dp(v.size(), 1);

           for (int i = 0; i < v.size(); ++i)
           {
               for (int j = 0; j < i; ++j)
               {
                   if(v[j] < v[i])
                   {
                      dp[i] = max(dp[i], dp[j]+1);
                   }
               }
           }
           for (auto it : dp)
           {
               cout << it << " ";
           }
           cout << endl <<  *max_element(dp.begin(), dp.end()) << endl;

           return 0;
      }

output

      1 2 3 3 4 
      4





LRU Cache Implementation
===============================================================================

.. code:: c++
