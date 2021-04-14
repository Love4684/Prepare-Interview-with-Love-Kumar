
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
