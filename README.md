# Calculator-Using-Java
import java.util.Scanner;
// import scanner from util package
class Main {
  public static void main(String[] args) {
    char operator;
    Double value1, value2, result;
    // create an object of Scanner class
    Scanner input = new Scanner(System.in);
    // we need to select which operation to be performed
    System.out.println("Choose an operator: +, -, *, /, ^ or % ");
    operator = input.next().charAt(0);
    // we need to take values from the user
    System.out.println("Enter first number");
    value1 = input.nextDouble();
    System.out.println("Enter second number");
    value2 = input.nextDouble();
    switch (operator) {
      case '+':
        result = value1 + value2;
        System.out.println(value1 + " + " + value2 + " = " + result);
        // it will perform addition operation for given values
        break;
      case '-':
        result = value1 - value2;
        System.out.println(value1 + " - " + value2 + " = " + result);
        // it will perform subtraction operation for given values
        break;
      case '*':
        result = value1 * value2;
        System.out.println(value1 + " * " + value2 + " = " + result);
        // it will perform mutiplication operation for given values
        break;
      case '/':
        result = value1 / value2;
        System.out.println(value1 + " / " + value2 + " = " + result);
        // it will perform division operation for given values
        break;
      case '^':
       result= Math.pow(value1,value2);
       System.out.println(value1 + " ^ " + (value2) + " = " + result);
       // it will perform  value1 powerof(value2)
       break;
      case '%':
       result = value1 % value2;
       System.out.println(value1 + " % " + value2 + " = " + result);
       // it is used to print the remainder
       break;  
      default:
        System.out.println("Invalid operator!");
        break;
    }
    input.close();
  }
}
