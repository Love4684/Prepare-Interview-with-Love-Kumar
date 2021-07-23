
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
