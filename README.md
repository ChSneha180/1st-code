# 1st-code
Spy number:-
Logic: A number where the sum of the digit is equal to the product of the digits.
####
code
import java.util.Scanner;
public class SpyNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int number = sc.nextInt();
        int sum = 0, product = 1, digit;
        int temp = number;
         while (temp > 0) {
            digit = temp % 10;        
            sum += digit;             
            product *= digit;         
            temp /= 10;               
        }
         if (sum == product) {
            System.out.println(number + " is a Spy Number.");
        } else {
            System.out.println(number + " is not a Spy Number.");
        }
    }
}
