

Write a program to search a key in a given set of elements using Binary search method and find the time complexity required to find the key

package program4;



import java.util.*;

public class binarysearch

{



	Static  int binary(int a[ ],int low,int high,key)

	 {

	    

	int mid;	   

 if(low>high)

	    {

		return -1;

		

	    }

	else

	  {

	

		mid=(low+high)/2;

		if(key==a[mid])

			return mid+1;

		else if(key>a[mid])

			return binary(a,mid+1,high,key);

		else

			return binary(a,low,mid-1,key);

	  }

        }

public static void main(String[] args) 

	{

	     int a[]=new int[100],i,n;

	    long start,end;

	

	    Scanner s1=new Scanner(System.in);

	    System.out.println("Enter the number of elements:");

	    n=s1.nextInt();



	    System.out.println("Enter sorted elements:");

	    for(i=0;i<n;i++)

	    {

	    	a[i]=s1.nextInt();	

	    }

	       

	

	System.out.println("Enter the key element:");

	    Int key=s1.nextInt();



	    long startTime = System.currentTimeMillis();

	  int x=  binary(a,0,n-1,key);

	    long endTime   = System.currentTimeMillis();

	    long totalTime = endTime - startTime;



	    System.out.println("\nThe sorted elements are:\n");

	    If(x==-1)

	    {

	    	System.out.println("key not found");

	    }

              Else

                {

	

	    System.out.println("key found at “+x);        

	}

}
