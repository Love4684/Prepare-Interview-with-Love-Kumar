
.. contents::
   :local:
   :depth: 2
   

Q.1
===============================================================================

.. image:: https://github.com/Love4684/Prepare-Interview-with-Love-Kumar/blob/main/bytedance/S.E/1.png

Reverse a Sentence using Stacks
------------

.. code:: c++

      #include<bits/stdc++.h>
      using namespace std;

      int main()
       {      
           string s;
           getline(cin, s);
           stack <string> st;
           for (int i = 0; i < s.length(); ++i)
           {  string w = "";
               while(s[i]!=' ' && i < s.length() )
               {
                  w += s[i];
                  i++;
               }
               st.push(w);
           }

           while(!st.empty())
           {
              cout << st.top() << " ";
              st.pop();
           }

          return 0;
      }

input

.. code:: c++

      RAM is a good boy


output

.. code:: c++

      boy good a is RAM 


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
    
Q.3
===============================================================================

.. image:: https://github.com/Love4684/Prepare-Interview-with-Love-Kumar/blob/main/bytedance/se/5.png    

cpp code
------------

`python <http://www.python.org>`_

.. code:: c++

      class Solution {
      public:
         void Parenthesis(int pos, int n, int open, int close, char str[], vector<string> &result)
      {

          if(close == n)
          {
              str[2*n] = '\0';
              result.push_back(str);
               return;
          }
          if(open < n)
          {
              str[pos] = '(';
              Parenthesis(pos+1, n, open+1, close, str, result);
          }
          if(close < open)
          {
              str[pos] = ')';
              Parenthesis(pos+1, n, open, close+1, str, result);
          }
      }
          vector<string> generateParenthesis(int n) {
              vector<string> result;
             char str[100];

          Parenthesis(0, n, 0, 0, str, result);
              return result;

          }
      };
