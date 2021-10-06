---
layout: default
---

Today we are going to perform the practical of access modifier which we learned in previous day blog

still let me recall all the modifiers for you 

- default
- public
- private
- protected


<b>Default</b>
```
class tut{
	public static void callme()
	{
		System.out.println("Default Access-Modifier");
	}
}

public class first {

	public static void main(String args[])
	{

		tut.callme();
		
	}

}

```
class "tut" will be accessible in this package only , let's create a new class with package name "tuts" 

```
package tuts;

*import com.yash.tut;*

public class test {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

	}

}


```
when we try to import "tut" class from package is gives us an error: <b> the type com.yash.tut is not visible </b>

<b>Public</b>
this type of class members are accessible to the outside-world , it means we can access inside the same package as well as
outside the package 

```
package com.yash;

public class first {

	public static void main(String args[])
	{

		System.out.println("This is a public class");
		
	}

}
```
let's creare a new class with package name "tuts" and then import the public class "frst" in it .

```
package tuts;

import com.yash.first;

public class test {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		first.main(args);

	}

}
```
this program will run successfully .

<b>Private</b>
These members are not even accessible in same package and not even in child class

```
package com.yash;


class tut{
	private static void callme()
	{
		System.out.println("This is a private class method");
	}
}

class tuts extends tut{
	void func() {
		tut.callme();
	}
}

public class first {

	public static void main(String args[])
	{

		System.out.println("This is a public class");
		tut.callme();
	}

}

```
<b>Protected</b>
These members are accessible in same package as well as a child class.

```
package com.yash;


class tut{
	protected static void callme()
	{
		System.out.println("This is a protected class method");
	}
}

class tester extends tut{
	static void func()
	{
	tester.callme();
	}
}
public class first {

	public static void main(String args[])
	{

		System.out.println("This is a public class");
		tut.callme();
		tester.func();
	}

}
```
now what if the child class is public , can we access the protected member outside the package ? answer is NO
but what if the class is public but method is protected ? can  we access it outside the package ?

```
//first.java
package com.yash;


public class first {
	
	protected static void disp() {
		System.out.println("Protected method in a public class");
	}

	public static void main(String args[])
	{

		System.out.println("This is a public class");
		first.disp();
	}

}

```
```
//test.java
package tuts;

import com.yash.first;

public class test extends first{

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		first.disp();
		

	}

}

```
and if you run test.java it will execute succesfully , because a public class is accessible outside the package and test class becomes the child class
and child class can access protected members , In this way we can access a protected member outside the package
