# Last-Permutation


import java.util.*;

public class HelloWorld
{
     public static void main(String []args)
     {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        String[] li=new String[n];
        for(int i=0;i<n;i++)
        {
            int p=sc.nextInt();
            li[i]=String.valueOf(p);
            
        }
        for(int i=0;i<n-1;i++)
        {
            for(int j=i+1;j<n;j++)
            {
                int m=Integer.parseInt(li[i]+li[j]);
                
                int e=Integer.parseInt(li[j]+li[i]);
                
                if(m<e)
                {
                    String temp=li[i];
                    li[i]=li[j];
                    li[j]=temp;
                }
            }
        }
        for(int i=0;i<n;i++)
        {
            System.out.println(li[i]);
        }
     }
}
