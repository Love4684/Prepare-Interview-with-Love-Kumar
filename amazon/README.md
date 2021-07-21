
# Online Assessment 1hr
Programmer Analyst - Amazon 
# Q.1) find output(margor)
        class HackerEarth {
     static String strVal;
    public static void main(String[] args)
    { HackerEarth h1 = new HackerEarth();
    strVal = h1.getstring("Program");
    System.out.print(" "+strVal);
    }
    public static String getstring(String str)
    {
    StringBuffer strBuf = new StringBuffer(str.length());
    for (int i=str.length() -1 ; i>0;i--)
    {
    strBuf.append(str.charAt(i));}
    return strBuf.toString();
    }
    }
# Q.2)  find output(HTRAEREKCAH)
    interface StrFunc{ String disp(String n);}
    class HackerEarth{

    public static void main(String args[]){

    StrFunc output = (str) -> { 
        String result = ""; 
        int a; 
        for(a = str.length()-1; a>= 0; a--) 
        result  = result + str.charAt(a);
        return result;
        };System.out.println(output.disp("HACKEREARTH"));
    }}
# Q.3) find output(6)
    class HackerEarth 
    { public static void main(String[] args) 
    {int sum = 0; int a = 3;
    while(sum++ < 3) 
    { int b = (1 + 2 * sum) % 3;
    switch(b)
    {default:
    case 0:
        a -= 1;
        break;
        case 1:
            a += 5;
            }
            }
            System.out.println(a);
    }
    }

# Q.4) [Convert given string to Palindrome with given substring](https://stackoverflow.com/questions/54959424/convert-given-string-to-palindrome-with-given-substring)
Given a String S1 and String S2. Convert string S1 to a palindrome string such S2 is a substring of that palindromic string. Only operation allowed on S1 is replacement of any character with any other character. Find minimum number of operations required.
# Q.5) [Size of the smallest subset with maximum Bitwise OR](https://www.geeksforgeeks.org/size-of-the-smallest-subset-with-maximum-bitwise-or/)
Given an array of positive integers. The task is to find the size of the smallest subset such that the Bitwise OR of that set is Maximum possible. 
# Q.6) Smallest Common Substrings 
You are glven two strings A and B made of lowercase English alphabets. Find the number of different pairs, (i,j),(k,l)), such that substring A[i….j] and B[k...I] are equal and the value of J-i+1 is minimum.

