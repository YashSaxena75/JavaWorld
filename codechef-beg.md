---
layout: default
---

```
package add;
import java.util.*;
import java.math.*;

public class code {
	static Scanner s = new Scanner(System.in);

	static void luckyfour(int r) {
		int c = 0;
		String a;
		
		for(int i=0; i<r ; i++) {
			a = s.next();
			for(int j=0;j<a.length();j++) {
				if(a.charAt(j)=='4') {
					c=c+1;
				}
			}
			System.out.println(c);
			c = 0;
		
		}
	}
	
	static void sfactorials(int r) {
		
		int num;
		int mult = 1;
		while( r >= 1) {
			num = s.nextInt();
			while ( num >= 1) {
				mult = mult*num;
				num = num - 1 ;
			}
			System.out.println(mult);
			mult = 1;
			r = r - 1;
		}
		
	}
	
	static void sofdigits(int r) {
		int num;
		int sum = 0;
		int rem;
		while( r >= 1) {
			num = s.nextInt();
			while ( num >= 1) {
				rem = num % 10;
				sum = sum + rem;
				num = num / 10;
			}
			System.out.println(sum);
			sum = 0;
			r = r - 1;
		}
	}
	
	static void revnumb(int r){
		
		int num ;
	    
	    while ( r >= 1)
	    {
	        int last = 0;
	        num = s.nextInt();
	        int x = Integer.parseInt(new StringBuilder(String.valueOf(num)).reverse().toString());
//	        while( num >= 1){
//	            last = num % 10;
//	            System.out.print(last);
//	            num = num/10;
//	        }
//	        System.out.println();
	        r = r - 1;
	        System.out.println(x);
	    }
				
	}
	
	
	
	static void fsqrt(int r) {
		while ( r >= 1) {
			int num = s.nextInt();
			System.out.println((int)Math.sqrt(num));
			r = r - 1;
			
		}
	}
	
	static void slar(int r) {
		
		int a[] = new int[r];
		int i;
		int f=0;
		int se=0;
		
		while ( r >= 1) {
			f = 0;
			se = 0;
			for(i=0;i<3;i++) {
				a[i] = s.nextInt();
			}
			
			for(i=0;i<3;i++)
			{
				if(a[i]>f)
				{
					se = f;
					f = a[i];
				}
				else if(a[i]>se && a[i]<f) {
					se = a[i];
				}
			}
			System.out.println(se);
			r = r - 1;
			
		}
		
		}
	
	static void game(int r) {
		
		int i;
		int rs =r;
		int a,b;
		int lead[] = new int[r];
		int lc[] = new int[r];
		int mc=0;
		
		while ( r >= 1) {
			
			a = s.nextInt();
			b = s.nextInt();
			
			if(a>b) {
				lc[mc] = 1;
				lead[mc] = a - b;
			}
			else if(b>a) {
				lc[mc] = 2;
				lead[mc] = b - a;
			}
			mc = mc + 1;
			r = r-1;
		}
			int larg = lead[0];
			int x = 0;
			for(i=1;i<rs;i++)
			{
				if(lead[i]>larg)
				{
					x = i; //1
					larg = lead[i]; //58
				}
			}
		
		System.out.printf("%d %d",lc[x],lead[x]);
			
	}
	
	

	// Main function
	public static void main(String[] args) {	
		int r = s.nextInt();
		//luckyfour(r);
		//sfactorials(r);
		//sofdigits(r);
		//revnumb(r);
		//fsqrt(r);
		//slar(r);
		//game(r);
		
	}
	
}


```
