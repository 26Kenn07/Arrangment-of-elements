# Arrangment-of-elements
How to arrange elements of array positive to negative

package pq;

import java.util.Scanner; 
  
class Matrix  
{   
    public static void main (String[] args)  
    { 
    	int arr[] = { 2 , -1 , 3 , -4 , 6 ,7 , -8 }; 
        int n = arr.length;
    	
    	
    	int key, j; 
        for(int i = 1; i < n; i++) 
        { 
            key = arr[i]; 
      
            
            if (key < 0) 
                continue; 
      
            j = i - 1; 
            while (j >= 0 && arr[j] < 0) 
            { 
                arr[j + 1] = arr[j]; 
                j = j - 1; 
            } 
       
            arr[j + 1] = key;
        }
        
        for(int i = 0 ; i < n ; i++)
        {	
        	System.out.print(arr[i]+" ");
        }
        
  
    } 
} 
  
