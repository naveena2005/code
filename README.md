// Control Statements - Kaprekar number
//   Jaffer wanted to excel in Math. He was learning about the Kaprekar number from Meena, his Maths teacher. She gave him a few random numbers and asked him to find out whether they are Kaprekar number or not.
// (Consider an n-digit number k. Square it and add the right n digits to the left n or n-1 digits. If the resultant sum is k, then k is called a Kaprekar number. For example, 9 is a Kaprekar number since 9^2 = 81 & 8 + 1 = 9, similarly, 297 is a Kaprekar number as 297^2 = 88209 & 88 + 209 = 297 ).
// Can you help Jaffer to write a program to find whether the given number is a Kaprekar number or not?

// Sample Input 0
// 45
  
// Sample Output 0
// Kaprekar Number
  
// Sample Input 1
// 23
  
// Sample Output 1
// Not a Kaprekar Number

import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int m=n;
        int c=0;
        while(m!=0){
            c++;
            m=m/10;
        }
        int sq=n*n;
        int p=(int)Math.pow(10,c);
        int l=sq/p;
        int r=sq%p;
        if(l+r==n)System.out.print("Kaprekar Number");
        else System.out.print("Not a Kaprekar Number");
    }
}
