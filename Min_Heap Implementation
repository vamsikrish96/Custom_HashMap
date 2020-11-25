// Implementation of Min Heap

package ps_1;
import java.util.*;
public class Heap_impl {

 static ArrayList<Integer> a = new ArrayList<Integer>();

 public static void main(String[] args) {
	
		Scanner inp = new Scanner(System.in);
		System.out.println("Enter the operations");
		
		for(int i =0;i<10;i++)
		{
			String oper = inp.next();
			
			if(oper.equals("Insert"))
			{
				
				int val = inp.nextInt();
				Insert(val);
				
				
			}
			
			else if(oper.equals("GetMin"))
			{
				if(a.size() == 0 )
				{
					System.out.println("EMPTY");
					
				}
				else
				{
					System.out.println(GetMin());
				}
				
				
			}
			
			else
			{
				if(a.size() != 0)
				{
				DelMin();
				}
				
			}
			
			
			
			System.out.println(a);
		}
		
}
 
 
 public static void Insert(int x) 
 {	
	a.add(x);
	
	int idx = a.size() - 1;
	if(a.size()!= 1)
	{
		while((idx>=0)&&(a.get((idx-1)/2) > a.get(idx)))
		{
			
			int temp = a.get(idx);
			a.set(idx,a.get((idx-1)/2));
			a.set(((idx-1)/2),temp);
			idx = (idx-1)/2;
			
		}
		
	}
	 
}
 
 
 public static int GetMin()
 {
	 return a.get(0);
	 
 }
	
 public static void DelMin()
 {	 int idx = 0;
	 a.set(0,a.get(a.size() - 1));
	 a.remove(a.size() - 1);
	 
	 int r_size = a.size();
	 
	 while(idx < r_size)
	 {
		 if((2*idx + 1 < r_size) && (2*idx + 2 < r_size))
		 {
			
			 if((a.get(2*idx + 1)<a.get(idx)) || (a.get(2*idx + 2)<a.get(idx)))
			 {
			 
				 if((a.get((2*idx) + 1) < a.get((2*idx) + 2)))
				 {
				 int temp = a.get(idx);
					a.set(idx,a.get((2*idx) + 1));
					a.set((2*idx) + 1,temp);
					idx = 2*idx + 1;
				 
				
				 }
			 
				 else
				 {
				 
				 int temp = a.get(idx);
					a.set(idx,a.get((2*idx) + 2));
					a.set((2*idx) + 2,temp);
					idx = 2*idx + 2;
				 
				 }
			 
			 // Taking the minimum condition.
			 
			 
			}
			 
			 else
			 {
				 break;
			 }
			 
		 
		 }
		 
		 
		 else if(2*idx + 1 < r_size)
		 {
			 
			 if(a.get(2*idx + 1)<a.get(idx))
			 {
				 int temp = a.get(idx);
					a.set(idx,a.get((2*idx) + 1));
					a.set((2*idx) + 1,temp);
					
				 
				 
			 }
			 idx = 2*idx + 1;
		}
			  
			
		else if(2*idx + 2 < r_size)
		{
			 if(a.get(2*idx + 2)<a.get(idx))
			 {
				 int temp = a.get(idx);
					a.set(idx,a.get((2*idx) + 2));
					a.set((2*idx) + 2,temp);
					
				 
				 
			 }
			 
			
			 idx = 2*idx + 2;
			
		}
			 
		else
		{
			
			break;
		}
		 
		 
	 }
	 
	 
}	

}



