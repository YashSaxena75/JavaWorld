---
layout: default
---

```
	static void vowel() {
		char str;
		str = s.next().charAt(0);
		if(str == 'A'||str=='a'||str == 'E'||str=='e'||str == 'I'||str=='i'||str == 'O'||str=='o'||str == 'U'||str=='u')
			System.out.println("Vowel");
		else
			System.out.println("Consonant");
	}
	
	static void appo(int r) {
		int a=0,b=0,c=0;
		
		while ( r >= 1) {
			
			a = s.nextInt();
			b = s.nextInt();
			c = s.nextInt();
			while(a!=b) {
				if ( c >= 1) {
					if(a>b)
					{
						b = b + 1;
						c = c - 1;
					}
					else if(b>a)
					{
						a = a + 1;
						c = c - 1;
					}
				}
				else
					break;
				System.out.println(Math.abs(a-b));
				
			}
			r = r - 1;
		}
	}
	
	static void skdwn( int r) {
		int a;
		while ( r >= 1) {
			a = s.nextInt();
			if(a==2010 || a==2015 || a==2016 || a==2017 || a==2019)
				System.out.println("HOSTED");
			else
				System.out.println("NOT HOSTED");
			
			r = r - 1;
		}
	}
	
	static void febfarm(int r) {
		int a=0,b=0;
		int flag = 0;
		int th = 0;
		while ( r>= 1 ) {
			
			a = s.nextInt();
			b = s.nextInt();
			int c = 0;
			c = a + b;
			c++; //8
			th = th + 1; //1
			while(flag!=2)
			{
				
				for(int i=2;i<c;i++) {
					if(c%i==0)
					{
						flag = 1;
						break;
					}
					else
						flag = 2;
				}
				
				if(flag==1)
				{
					c = c + 1; //9
					th = th + 1; //2
				}
				
			}
			
			System.out.println(th);
			th = 0;
			flag = 0;
			r = r - 1;
			c = 0;
		}
	}
	
	static void digitco() {
		
		int num = s.nextInt();
		
		String str = Integer.toString(num);
		if(str.length()==1)
			System.out.println("1");
		else if(str.length()==2)
			System.out.println("2");
		else if(str.length()==3)
			System.out.println("3");
		else
			System.out.println("More than 3");
	}
	
	
	static void pyra(int r) {
		int a=0,c=0;
		
		while ( r >= 1) {
			a = s.nextInt();
			for (int i=1;i<=a;i++) {
				if(a>=1 && a>=i)
				{
					a = a - i; //2
					c = c + 1; //1
				}
				else
					break;
			}
			
			r = r - 1;
			System.out.println(c);
			c = 0;
		}
	}
```
