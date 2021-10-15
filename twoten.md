---
layout: default
---

```
class Codechef
{
    static Scanner s = new Scanner(System.in);
  	static void tten(int r) {
		long a;
		int flag = 0,fl = -1;
		long c = 0;
		long ac = 0;
		while ( r >= 1) {
			ac = 1;
			a = s.nextLong();
			ac = a;
			while(ac<=1000000000) {
				if ( ac>=5)
				{
					if ( ac%10==0)
					{
						flag = 1;
						break;
					}
					else
					{
						ac = ac*2;
						c = c + 1;
					}
				}
				else
				{
					c = -1;
					flag =1;
					break;
				}
			}
			if(flag==1)
				System.out.println(c);
			else
				System.out.println(fl);
			c = 0;
			r = r - 1;
		}
		
	}
	public static void main (String[] args) throws java.lang.Exception
	{
		// your code goes here
		int r = s.nextInt();
		tten(r);
	}
}

```
