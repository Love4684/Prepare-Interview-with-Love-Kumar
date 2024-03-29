.. contents::
   :local:
   :depth: 3

Infosys Interview Questions
===============================================================================

product of all prime number less than given number
----------------------------------------------------

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
----------------------------------------------------

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
----------------------------------------------------

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
----------------------------------------------------

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
----------------------------------------------------

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

.. code:: c++


      1 2 3 3 4 
      4

Longest Increasing Subsequence NlogN approach
----------------------------------------------------

.. code:: c++


      #include<bits/stdc++.h>
      using namespace std;

      int main()
       {     
           vector<int> v = {3, 10, 2, 1, 20};
           vector<int> dp;
           dp.push_back(v[0]);

           for (int i = 1; i < v.size(); ++i)
           {
               if(v[i] > dp.back())
               {
                  dp.push_back(v[i]);
               }
               else
               {
                  int ind = upper_bound(dp.begin(), dp.end(), v[i]) - dp.begin();
                  dp[ind] = v[i];
               }
           }
           for (auto it : dp)
           {
               cout << it << " ";
           }
           cout << endl <<  dp.size() << endl;

           return 0;
      }

output

.. code:: c++

      1 10 20 
      3



Palindromic Substring
----------------------------------------------------

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;
      int LPS(string str)
      { int n = str.size();
          int maxlength = 1, start;
          int count = n;
          bool a[n][n];
          memset(a, 0, sizeof(a));
          for (int i = 0; i < n; ++i)
          a[i][i] = true;

          for (int i = 0; i < n-1; ++i)
          {
              if(str[i] == str[i+1])
              {
                  a[i][i+1] = true; count++;
                  start = i;
                  maxlength = 2;
              }
          }

          for(int k = 3; k <= n; k++)
          {
              for (int i = 0; i <= n-k; ++i)
          {int j = k+i-1;
              if(a[i+1][j-1] && str[i] == str[j])
              {
                  a[i][j] = true; count++;
                  start = i;
                  if(k>maxlength)
                  maxlength = k;
              }
          }
          }
          cout << "total Palindromic Substring is : " << count << endl;
          cout << "longest Palindromic Substring is : " << str.substr(start, maxlength) << endl;
          return maxlength;

      }
      int main()
      {
          string str = "ABCDCBE";
         int l = LPS(str);
         cout << "maxlength of Palindromic Substring is : " <<  l;

          return 0;
      }

output

.. code:: c++

      total Palindromic Substring is : 9
      longest Palindromic Substring is : BCDCB
      maxlength of Palindromic Substring is : 5


Segregate Even and Odd numbers
----------------------------------------------------

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;
      int main()
      {
          int arr[7] = {6, 5, 3, 4, 2, 1, 4};
          int i = 0;
          int j = 6;
          while(i<j)
          {
              while((arr[i]&1) == 0)
              {
                  i++;
              }
              while((arr[j]&1) == 1)
              {
                  j--;
              }
              swap(arr[i], arr[j]);
              i++; j--;
          }
          for (int i = 0; i < 7; ++i)
          {

              cout << arr[i] << " ";
          }
      }

output

.. code:: c++

      6 4 2 4 3 1 5

Given a number, find the next smallest palindrome
----------------------------------------------------

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;

      string nxtpl(string num)
      {
          int n = num.size();
          string str = num;
          for (int i = 0, j = n-1; i < j; ++i, --j)
          {
              str[j] = str[i];
          }
          if(str > num)
              return str;
          else
          {
              int mid = n/2;
              if((n&1) == 0) mid--;
              while(mid>=0)
              {
                  if(str[mid] < '9')
                  {
                      str[mid]++;
                      break;
                  }
                  else
                  {
                      str[mid] = '0';
                      mid--;
                  }
              }
              if(mid==-1 && str[0] == '0')
              {
                  n++;
                  str = '1' + str;
              }
              for(int i = 0, j = n-1; i < j; i++, j--)
              {
                  str[j] = str[i];
              }
              return str;
          }
      }

      int main()
      {
          string s = "4321";
          string np = nxtpl(s);
          cout << np;
          return 0;
      }

Given an array A[] and a number x, check for pair in A[] with sum as x
----------------------------------------------------

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;

      void findpair(std::vector<int> v, int sum)
      {
          sort(v.begin(), v.end());
          int l = 0;
          int r = v.size() - 1;
          while(l<r)
          {
              if((v[l] + v[r]) == sum)
              {
                  cout << v[l] << " " << v[r];
                  break;
              }
              if((v[l] + v[r]) < sum)
                  l++;
              else
                  r--;
          }
      }

      int main()
      {
         std::vector<int> v = {4, 5, 6, 7, 5, 4, 4};
         int sum = 10;
         findpair(v, sum);
         return 0;
      }

Method 2: Hashing.
------------------

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;

      void findpair(std::vector<int> v, int sum)
      {
          unordered_set<int> s;
          for (int i = 0; i < v.size(); ++i)
          {
              int temp = sum-v[i];
              if(s.find(temp) != s.end())
                  cout << temp << " " << v[i] << endl;
              s.insert(v[i]);
          }
      }

      int main()
      {
         std::vector<int> v = {1, 4, 45, 6, 10, 8};
         int sum = 16;
         findpair(v, sum);
         return 0;
      }

Shortest path in a Binary Maze
----------------------------------------------------

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;
      int dir[8][2] = {{1, 1}, {1, -1}, {-1, 1}, {1, 0}, {0, 1}, {-1, -1}, {0, -1}, {-1, 0}};
      struct point
      {
          int x;
          int y;
          int count;
      };
      class solution
      {
      public:
          int shortestPathBinaryMatrix(vector<vector<int>> &grid)
          {
              if(grid[0][0] == -1) return -1;
              int row = grid.size();
              int col = grid[0].size();
              queue<point> q;
              q.push({0, 0, 1});
              grid[0][0] = -1;
              while(!q.empty())
              {
                  point p = q.front();
                  q.pop();
                  if(p.x == row-1 && p.y == col-1)
                      return p.count;
                  for (int i = 0; i < 8; ++i)
                  {
                      int x = p.x + dir[i][0];
                      int y = p.y + dir[i][1];
                      if(x>=0 && x<row && y>=0 && y<col && grid[x][y]==0)
                      {
                          q.push({x, y, p.count+1});
                          grid[x][y] = -1;
                      }
                  }
              }
              return -1;
          }

      };
      int main(){
         vector<vector<int>> v = {{0,0,0},{1,1,0},{1,1,0}};
         solution ob;
         cout << (ob.shortestPathBinaryMatrix(v));
      }

Next Greater Element
----------------------------------------------------

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;
      void fun(int arr[], int n)
      {int j;
          for (int i = 0; i < n; ++i)
          {
              for ( j = i+1; j < n; ++j)
              {
                  if(arr[i] < arr[j])
                  {
                       arr[i] = arr[j];
                      break;
                  }  
              }
              if(j==n)
              {
                  arr[i] = -1;
              }
          }  
          for (int i = 0; i < n; ++i)
          {
              cout << arr[i] << " ";
          }
      }
      int main()
      {
         int arr[]= {4, 5, 30, 2, 25};
         // 5 25 25 -1
         fun(arr, 5);
         return 0;
      }

output

.. code:: c++

      5 30 -1 25 -1 
