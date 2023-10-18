# interviewQuestion

Q.1) Write a program to calculate the maximum product from the 4 element of an array

Soln :

import java.util.*;
class HelloWorld {
    public static void main(String[] args) {
        int temp,sum=1;
        Scanner sc=new Scanner(System.in);
        int arr[]=new int[5];
        for(int i=0;i<arr.length;i++){
            arr[i]=sc.nextInt();
        }
        // for(int i=0;i<arr.length;i++){
        //     System.out.print(arr[i]+" ");    
        // }
        
        for(int i=0;i<arr.length;i++){
            for(int j=i+1;j<arr.length;j++){
                if(arr[i]<arr[j]){
                    temp=arr[i];
                    arr[i]=arr[j];
                    arr[j]=temp;
                }
            }
        }
        for(int i=0;i<arr.length;i++){
            System.out.println();
            // System.out.print(arr[i]+" ");    
        }
        
        for(int i=0;i<4;i++){
            sum=sum*arr[i];
        }
        System.out.println(sum);
    }
}
