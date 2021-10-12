---
layout: default
---

```

static void lap(int r) {
		
		String str;
		while( r >= 1) {
			str = s.next();
			int len = str.length();
			int lc = len;
			if(len%2==0)
			{
				len = len - 1;
				len = len/2;
				int i=0,j=0;
				char left[] = new char[len+1];
				char right[] = new char[len+1];
				
				for(i=0;i<=len;i++) {
					left[i] = str.charAt(i);
				}
				
				for(i=i;i<lc;i++) {
					right[j] = str.charAt(i);
					j = j + 1;					
				}
				
				Arrays.sort(left);
				Arrays.sort(right);
				
				String ri = String.copyValueOf(right);
				String le = String.copyValueOf(left);
				
				
				if(ri.equals(le))
					System.out.println("YES");
				else
					System.out.println("NO");
			}
			
			else
			{
				len = len/2;
				int i=0,j=0;
				char left[] = new char[len];
				char right[] = new char[len];
				
				for(i=0;i<len;i++) {
					left[i] = str.charAt(i);
					
				}
				for(i=i+1;i<lc;i++) {
					right[j] = str.charAt(i);
					j = j + 1;					
				}
				Arrays.sort(left);
				Arrays.sort(right);
				
				String ri = String.copyValueOf(right);
				String le = String.copyValueOf(left);
				
				
				if(ri.equals(le))
					System.out.println("YES");
				else
					System.out.println("NO");
			}
			
		r = r - 1;	
			
		}
	}


```

Today we are going to look a very interesting problem we have from codechef "Lapindrome" . where we have to check if the two halves of a String
contains the same character with same number of frequency or not .

for ex: haha is palindrome because two halves "ab" and "ab" are equal in terms of character and their frequency .

there are two ways to solve this challenge , either we can use inbuilt functions to divide the string or we can code this part also ( this is what
I did ) and then took some help from the internet and found that after dividing the string just sort them and compare them

we started with finding the length of the string , if the length is of even number then we have to follow the if part otherwise else part
because "haha"s two halves (4/2)=2 will be "ha" and "ha" whereas two halves for a odd length string like this "abcde" will be "ab" and "de"
we have two char array , one to store left hand side characters and one is to store right hand side characters , how we are going to define their
storage size now ? 

if the length is even say "4" then len = len - 1 i.e 3 and then len = 3/2 = 1 , so we are going to define the array of length , len + 1

<b>char left[] = new char[len+1];
char right[] = new char[len+1];</b>

now for odd number length strings , we have len = len/2 and array size will be len

<b>char left[] = new char[len];
char right[] = new char[len];</b>

now acording to the string length , copy the left hand side element to keft[] and right side element to right[] then sort them
using <b>Arrays.sort()</b> then copy the elements of both array to a string using , <b>String ri = String.copyValueOf(right)</b> , same for left[] array
and then compare the two strings using equals(() functions like this

if(ri.equals(le))
	System.out.println("YES");
else
	System.out.println("NO");
	
complexity here will be O(n) if we ignore the starting while loop , that loop is because of number of test cases.
