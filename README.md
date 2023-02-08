This is a Solution for LeetCode

**Question is-- Reverse String ||**

Given a string s and an integer k, reverse the first k characters for every 2k characters counting from the start of the string.

If there are fewer than k characters left, reverse all of them. If there are less than 2k but greater than or equal to k characters, then reverse the first k characters and leave the other as original.

Example-
Input: s = "abcdefg", k = 2
Output: "bacdfeg"

```
Solution:-
  #include<bits/stdc++.h>
  using namespace std;

  string rev(string s, int k){
      int len = s.length();
      for(int i = 0; i< s.size(); i+=2*k){
          if(i+k>len){
             break;
          }
          reverse(s.begin()+i, s.begin()+i+k);
      }
      return s;
  }

  int main(){
      string s;
      cout<<"Enter the any char: ";
      cin>>s;
      int k = 2;
      cout<<rev(s,k);
      return 0;
  }
  ```
