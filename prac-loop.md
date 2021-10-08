---
layout: default
---
package prac;

public class pracset {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		// Question-1
		int n = 4 ;
		for(int i=n;i>=1;i--)
		{
			for(int j=0;j<i;j++) {
			System.out.print("*");
			
			}
			System.out.println();
		}
		
		// Question-2
		int en = 10 ;
		int i=1;
		int sum = 0;
		
		while(i<=en) {
			
			sum = sum + (2*i);
			i = i + 1;
		}
		
		System.out.printf("Sum of first %d even numbers is %d",en,sum);
		System.out.println();
		
		// Question-3
		n = 3;
		i = 1;
		while(i<=10) {
			System.out.println(i*3);
			i= i + 1;
		}
		System.out.println();
		
		// Question-4
		n = 10;
		i = 10;
		while(i>=1) {
			System.out.println(i*n);
			i = i-1;
		}
		System.out.println();
		
		// Question-5
		n = 4;
		int fact = 1;
		while(n>0) {
			
			fact = fact*(n);
			n = n-1;
		}
		System.out.println(fact);
		System.out.println();
		
		// Question-6
		n = 4;
		for(i=0;i<n;i++) {
			for(int j=0;j<i+1;j++)
			{
			System.out.print("*");
			}
			System.out.println();
		}
		
		
		System.out.println();
		
		// Question-7
		n = 4;
		for(i=0;i<n;i++)
		{
			for(int j=0;j<i+1;j++)
			{
			System.out.print("*");
			}
			System.out.println();
		}
		
		n = 3;
		for(i=0;i<n;i++) {
			for(int j=n;j>i;j--) {
			System.out.print("*");
			}
			System.out.println();
		}
			
	}
	

}
