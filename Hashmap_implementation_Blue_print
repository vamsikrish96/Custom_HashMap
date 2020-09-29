package problem_solving_2;
import java.util.*;
public class Custom_Hash_Map {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Hmap hm = new Hmap();
		
		hm.Put_key(1, 10);
		hm.Put_key(2, 20);
		hm.Put_key(3, 30);
		
		System.out.println(hm.Get_key(1));
}

// Entry Level object to be created

static class Entry{

	int key;
	int value;
	int hash_key;
	Entry next;
	
	Entry(int x , int y)
	{
		key = x;
		value = y;
		next = null;
	}
}

public static class Hmap{
	
	int hm_size = 16;
	ArrayList<Entry> a; 
	Hmap()
	{   
		a =  new ArrayList<Entry>(hm_size);
		for(int i = 0;i<hm_size;i++)
		{
			a.add(null);
		}
	
		
	}
	
	int  Size()
	{
		return a.size();
	}
	
	void Put_key(int key,int value)
	{
		Entry temp = new Entry(key,value);
		
		temp.hash_key = ((Integer)key).hashCode();
		
		int pos = temp.hash_key%hm_size;
		
		if(a.get(pos) == null)
		{
			a.set(pos,temp);	
		}
		else
		{
			Entry tx = a.get(pos);
			while(tx != null)
			{
				tx = tx.next;
			}
			
			tx = temp;
		}
	}
	
	int Get_key(int key)
	{
		int temp = ((Integer)key).hashCode();
		int pos = temp%hm_size;
		
		Entry ans = a.get(pos);
		
		while((ans.key != key) && (ans != null))
		{
			ans = ans.next;
		}
		
		if(ans.hash_key == temp)
		return ans.value;
		else
		return -1;
	}
	
	void clearAll()
	{
		for(int i = 0;i<hm_size;i++)
		{
			a.add(null);
		}
	
		System.out.println("Cleared the whole map");
	}
	
	
	
	
	
}


}
