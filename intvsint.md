---
layout: default
---

<center><h2 style="color:#66FF33">int vs Integer</h2></center>

we all are quite familiar with int data type , it is a primitive data type that we have used in different languages like , C C++ Java etc.
we have used int for different operations , especially when we start with a program to add two numbers , right ? but we haven't used
"Integer" Data type many times or some of us like me get to know for the very first time. 
let's look at a simple program

```
public class hello{
  
  public static void main(String[] args) {
      int a = 8;
      Integer b = 8;
      
      System.out.println(a);
      System.out.println(b);
  }
}

```

this program will print 8 both the times , so what's the difference between these two and which one should I use ? well , it depends on the 
problem scenario , you can use "int" wherever  you want to use , but "int" is a primitive data type and we can't perform much operation on it
where as "Integer" is a wrapper class which provides us some extra functions to help us more while coding , let's see how

```
	static void ex1() {
		
		int a[] = {1,3,4,2};
		int b[] = {1,2,5};
		
		int el = 2;
		int flag = 0 ;
		
		for(int i=0;i<3;i++)
		{
			for(int j=0;j<4;j++)
			{
				if(b[i]==a[j])
					flag = flag + 1;
			}
		}
		
		if(flag==3)
			System.out.println("all elements are present");
		else
			System.out.println("1 or more than element is missing");
		
	}
```
This code will take around O(n^2) time complexity , now let's try this in some other way

```
static void ex2() {
		
		Integer a[] = {1,3,4,2};
		Integer b[] = {1,2,5};
		
		int el = 2;
		int flag = 0 ;
		
		for(int i=0;i<3;i++)
		{
			if(Arrays.asList(a).contains(b[i]))
				flag = flag + 1 ;
		}
		if(flag==3)
			System.out.println("all elements are present");
		else
			System.out.println("1 or more than element is missing");
		
	}

```
now this code is using "Integer" wrapper class , which provides us more options to perform on the data .
we have used only one for loop , but I can't say how this <b style="color:#66FF33">Array.asList().contains()</b> works , so we can't 
say that time ecomplexity here is O(n) but definelty time must be less than the first code where we have used
two for loops
So data manipulation becomes more easy with wrapper classes 

I tried running both the codes and found that <b style="color:#66FF33">code execution time was almost similar</b> , there was a very minor difference , probably
we can ignore it 

but yes wrapper classes more functionality than primitive data types 
