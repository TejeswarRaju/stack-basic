# stack-basic
reverse order.  Reverse the order of the items stored in the stack. Option 7: print the result of the operation at the top of the stack Option 8: Remove the item from the top of the stack, effectively deleting it. Print author info (prints your name and id)
package com.internshala.recursion;


import java.util.Scanner;
import java.util.Stack;

import static java.util.Collections.reverse;

public class Main {
    public static void main(String[] args) {
        String name = ("Tejeswar Raju Vempalli");
        int csuId =2816828;
        System.out.println(name);
        System.out.println("Csu Id:"+ csuId);
        Stack<Integer> stack1 = new Stack<>();
        Stack<Integer> stack2= new Stack<>();
        Scanner scan = new Scanner(System.in);
        System.out.println("Enter your first Number:");
        int num1 = scan.nextInt();
        System.out.println("Enter your second Number:");
        int num2 = scan.nextInt();
        stack1.push(num1);
        stack1.push(num2);
        System.out.println("Enter your operation Number:");
        int operation = scan.nextInt();
        int result = 0;
        if (operation == 1) {
            result = num1 + num2;
            System.out.println("your result:" +result);
        }
          else  if (operation == 2) {
                result = num1 - num2;
                System.out.println("your result:" +result);
            } else if (operation == 3) {
                result = num1 * num2;
                System.out.println("your result:" +result);
            } else if (operation == 4) {
                result = num1 / num2;
                System.out.println("your result:"+ result);
            } else {
                System.out.println("you entered a wrong Operation:");
            }
        stack1.push(result);
        System.out.println("your stack1:" + stack1);
        stack2.push(stack1.pop());
        stack2.push(stack1.pop());
        stack2.push(stack1.pop());
        System.out.println("Your stack2:" +stack2);
        System.out.println("Removed Element from stack:"+stack2.pop());
        }


}
