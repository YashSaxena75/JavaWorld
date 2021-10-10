---
layout: default
---

```
static void game(int r) {
		
		int a,b,m=0,n=0,d1=0,d2=0,lead1=0,lead2=0;
		while ( r >= 1) {
			
			a = s.nextInt();
			b = s.nextInt();
			m = m+a;
			n = n+b;
			 if (m>=n)
		        {
			        d1=m-n;
		        }
		        if (m<n)
		        {
		            d2=n-m;
		        }
		        if (d1>lead1)
		        {
		            lead1=d1;
		        }
		        if (d2>lead2)
		        {
		            lead2=d2;
		        }
		        
		        r = r - 1;
	
		}
		
		 if (lead1>lead2)
			    System.out.printf("1 %d",lead1);
		    if (lead2>lead1)
		    	System.out.printf("2 %d",lead2);
		
			
	}
	
	static void chelp(int r) {
		
		int a;
		while ( r >= 1) {
			a = s.nextInt();
			if(a < 10)
				System.out.println("Thanks for helping Chef!");
			else
				System.out.println("-1");
			
			r = r - 1;
		}
	}
	
	static void rop(int r) {
		int a,b;
		while ( r >= 1) {
			a = s.nextInt();
			b = s.nextInt();
			if(a>b)
				System.out.println(">");
			else if(b>a)
				System.out.println("<");
			else
				System.out.println("=");
			
			r = r - 1;
		}
	}
	
	static void cup(int r) {
		int a=0;
		int left = 0; 
		while ( r >= 1) {
			a = s.nextInt();
			if(a<=2) {
				System.out.println(a);
			}
			else {
				left = a/2;
				left = 1 + left;
				System.out.println(left);
				
			}
			
			r = r - 1;
		}
	}

	static void vtri(int r) {
		
		int a=0,b=0,c=0;
		while ( r >= 1) {
			a = s.nextInt();
			b = s.nextInt();
			c = s.nextInt();
			if(a+b+c==180)
				System.out.println("YES");
			else
				System.out.println("NO");
			
			r = r - 1;
		}
	}
	
	static void incdec(int r) {
		
		int a = 0;
		while( r >= 1) {
			a = s.nextInt();
			if(a%4==0)
				System.out.println(a+1);
			else
				System.out.println(a-1);
			
			r = r - 1;
		}
	}

```

