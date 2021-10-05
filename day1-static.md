---
layout: default
---
<center><b><pre> Why we use Static Keyword ?</pre></b></center>

if we declare a function with static keyword then we don't need an object to be created and then 
call the function


```
public class first {

	public static void main(String args[])
	{
		System.out.println("Static");

	}

}
```
In this code we have not created object of class "first" and still the main method was executed 
Now check this program

```
class tut{
	public void callme()
	{
		System.out.println("Non-Static Method");
	}
}

public class first {

	public static void main(String args[])
	{
		System.out.println("Static");
		tut t = new tut();
		t.callme();
		
	}

}

```
for this program I have declared two classes , one is public and is not public , and inside tut class 
we have a non-static method and to call/execute this method we have created class object
but what if I define this function with <b>static</b> keyword , do I still need to create 
a class object ?

```
class tut{
	public static void callme()
	{
		System.out.println("Non-Static Method");
	}
}

public class first {

	public static void main(String args[])
	{
		System.out.println("Static");
//		tut t = new tut();
//		t.callme();
		
	}

}
```
but this thing didn't worked at all , why ? 
because tut class is not public and to access it's members we need an object 
so the question is why we need <b>static</b> keyword if we can use it only inside the public class 
and if you are thinking to create two public classes in a single source file , then sorry you can't do this

but wait .... the above explanation for static keyword is partially/completely wrong , that you have to decide

look at this code

```
class tut{
	public static void callme()
	{
		System.out.println("Non-Static Method");
	}
}

public class first {

	public static void main(String args[])
	{
		System.out.println("Static");
//		tut t = new tut();
//		t.callme();
		tut.callme();
		
	}

}
```
and it worked perfectly , right ? so this is what it means when we say " we don't have to create an object to call static methods " ,
we can directly call them with classname.method_name();
and if you remove the <b>static</b> keyword from the above program then you will get this error: "Cannot make a static reference to the non-static method"
