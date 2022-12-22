//import java.util.Scanner;
//
//public class AsseignmentD3 {
//    public static void main(String[] args) {
//        Scanner in = new Scanner(System.in);
//        int a, b, c = 0;
//        System.out.println("enter three numbers");
//        a = in.nextInt();
//        b = in.nextInt();
//        c = in.nextInt();
//        max(a, b, c);
//        min(a, b, c);
//    }
//    static void min(int x, int y, int z) {
//        if (x<y && x<z){
//            System.out.println("Minimum value is "+x);
//        }
//        if (y<z && y<x){
//            System.out.println("Minimum value is "+y);
//        }
//        if (z<x && z<y){
//            System.out.println("Minimum value is "+z);
//        }
//    }
//    static void max(int x, int y, int z){
//        if (x>y && x>z){
//            System.out.println("Maximum value is "+x);
//        }
//        if (y>z && y>x){
//            System.out.println("Maximum value is "+y);
//        }
//        if (z>x && z>y){
//            System.out.println("Maximum value is "+z);
//        }
//        question two

//        int n = in.nextInt();
//        if (n % 2 == 0) {
//            System.out.println("its an even");
//        } else {
//            System.out.println("its an odd");
//        }
//          question three.
//        System.out.println("enter your age");
//        int age = in.nextInt();
//        if (age >= 18) {
//            System.out.println("you are eligible");
//        } else {
//            System.out.println("you aren't eligible");
//        }
//        question four.
//        System.out.println("enter first number");
//        int num1 = in.nextInt();
//        System.out.println("enter second number");
//        int num2 = in.nextInt();
//        int sum = num1 + num2;
//        System.out.println("sum of two is: " +sum);

//        question five.
//        System.out.println("enter first number");
//        int num1 = in.nextInt();
//        System.out.println("enter second number");
//        int num2 = in.nextInt();
//
//        calproduct(num2, num1);
//    }
//        static void calproduct(int x, int y) {
//        int result = 0;
//        result = x * y;
//            System.out.println("calculate the product:" + result);
//        }
//          question six
////        System.out.println("enter the area: ");
//        int radius = in.nextInt();
//        //formula to calculate area of circle
//        double area = Math.PI * (radius * radius);
//        System.out.printf("Area is: %.2f", area);
//
//        //formula to calculate circumference of circle
////        System.out.println("enter the Circumference: ");
//        double circumference= Math.PI * 2*radius;
//        System.out.printf( "\nCircumference is: %.2f",circumference) ;

//        error this code is wrong.
//        System.out.println("enter a number");
//        int num = in.nextInt();
//
//    }
//    static void tokennum(int num) {
//        if (num == 2) {
//            System.out.println("is prim number");
//        } else {
//            if (num % 2) {
//                System.out.println("is not prim");
//            }
//        }
//              question seven.

//        // A school method based JAVA program
//// to check if a number is prime
//        class GFG {
//
//            static boolean isPrime(int n)
//            {
//                // Corner case
//                if (n <= 1)
//                    return false;
//
//                // Check from 2 to n-1
//                for (int i = 2; i < n; i++)
//                    if (n % i == 0)
//                        return false;
//
//                return true;
//            }
//
//            // Driver Program
//            public static void main(String args[])
//            {
//                if (isPrime(11))
//                    System.out.println(" true");
//                else
//                    System.out.println(" false");
//                if (isPrime(15))
//                    System.out.println(" true");
//                else
//                    System.out.println(" false");
//            }
//        }
//            question eight
//        int count, i;
//        float totalmarks =0, percentage, average;
//        Scanner Scanner;
//        System.out.println("enter number of subjects");
//        count = in.nextInt();
//        System.out.println("enter marks of " + count + "subject");
//        for (i = 0; i < count; i++) {
//            totalmarks += in.nextInt();
//        }
//        System.out.println("Total MArks : " + totalmarks);
//        // Each subject is of 100 Marks
//        percentage = (totalmarks / (count * 100)) * 100;
//
//        /* Printing grade of a student using switch case statement */
//        switch ((int) percentage / 10) {
//            case 9:
//                System.out.println("Grade : A+");
//                break;
//            case 8:
//            case 7:
//                System.out.println("Grade : A");
//                break;
//            case 6:
//                System.out.println("Grade : B");
//                break;
//            case 5:
//                System.out.println("Grade : C");
//                break;
//            default:
//                System.out.println("Grade : D");
//                break;
//        }
//
//          question nine
//  int i,fact=1;
//          int number=5;//It is the number to calculate factorial
//          for(i=1;i<=number;i++){
//          fact=fact*i;
//          }
//          System.out.println("Factorial of "+number+" is: "+fact);

//          question ten
//      public static int oneDigit(int num) {
//
//        if ((num >= 0) && (num < 10))
//        return 1;
//        else
//        return 0;
//        }
//
//      public static int isPalUtil
//        (int num, int dupNum) throws Exception {
//
//        // base condition to return once we
//        // move past first digit
//        if (num == 0) {
//        return dupNum;
//        } else {
//        dupNum = isPalUtil(num / 10, dupNum);
//        }
//
//// Check for equality of first digit of
//// num and dupNum
//        if (num % 10 == dupNum % 10) {
        // if first digit values of num and
        // dupNum are equal divide dupNum
//        // value by 10 to keep moving in sync
//        // with num.
//        return dupNum / 10;
//        } else {
//        // At position values are not
//        // matching throw exception and exit.
//        // no need to proceed further.
//        throw new Exception();
//        }
//
//        }
//
//      public static int isPal(int num)
//        throws Exception {
//
//        if (num < 0)
//        num = (-num);
//
//        int dupNum = (num);
//
//        return isPalUtil(num, dupNum);
//        }
//
//     public static void main(String args[]) {
//
//        int n = 1242;
//        try {
//        isPal(n);
//        System.out.println("Yes");
//        } catch (Exception e) {
//        System.out.println("No");
//        }
//        n = 1231;
//        try {
//        isPal(n);
//        System.out.println("Yes");
//        } catch (Exception e) {
//        System.out.println("No");
//        }
//
//        n = 12;
//        try {
//        isPal(n);
//        System.out.println("Yes");
//        } catch (Exception e) {
//        System.out.println("No");
//        }
//        n = 88;
//        try {
//        isPal(n);
//        }
//        System.out.println("Yes");
//        } catch (Exception e) {
//        System.out.println("No");
//        }
//
//        n = 8999;
//        try {
//        isPal(n);
//        System.out.println("Yes");
//        } catch (Exception e) {
//        System.out.println("No");
//        }
//        }
//    }
//}
