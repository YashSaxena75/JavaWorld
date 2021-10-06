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

_import com.yash.tut;_

public class test {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

	}

}


```
when we try to import "tut" class from package is gives us an error: <b> the type com.yash.tut is not visible </b>
