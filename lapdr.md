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
