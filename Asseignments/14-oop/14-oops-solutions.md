
<!-- question one: Inheritance one -->
class waly{
    void walk(){
        System.out.println("I am walking");
    }
}
class Bird extends Animal{
	void fly(){
		System.out.println("I am flying");
	}
    void sing(){
        System.out.println("I am singing");
    }
}
public class Solution{
   public static void main(String[] args){

      Bird bird = new Bird();
      bird.walk();
      bird.fly();
   }
}

<!-- question two: inheritance two -->

class Arithmetic{
    public int add(int a, int b){
        int sum = a + b; 
        return sum;
    }
}

class Adder extends Arithmetic{  
    public int callAdd(int a, int b){
        return add(a, b);
    }
}
public class Solution{
    public static void main(String []args){
        // Create a new Adder object
        Adder a = new Adder();
        
        // Print the name of the superclass on a new line
        System.out.println("My superclass is: " + a.getClass().getSuperclass().getName());	
        
        // Print the result of 3 calls to Adder's `add(int,int)` method as 3 space-separated integers:
        System.out.print(a.add(10,32) + " " + a.add(10,3) + " " + a.add(10,10) + "\n");
     }
}

<!-- question three: Java Abstract class -->

abstract class Buug {
   String title;
   abstract void setTitle(String s);
   String getTitle()
   {
      return title;
   }
   
}

class MyBook extends Book {
    
    @Override
    void setTitle(String s){
        this.title = s;
    }
    
}
public class Main{
	
	public static void main(String []args){
		//Book new_novel=new Book(); This line prHMain.java:25: error: Book is abstract; cannot be instantiated
		Scanner sc=new Scanner(System.in);
		String title=sc.nextLine();
		MyBook new_novel=new MyBook();
		new_novel.setTitle(title);
		System.out.println("The title is: "+new_novel.getTitle());
      	sc.close();
		
	}
}

<!-- question four: Java Interface -->
class Solution{
    public static void main(String []args){
        MyCalculator my_calculator = new MyCalculator();
        System.out.print("I implemented: ");
        ImplementedInterfaceNames(my_calculator);
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        System.out.print(my_calculator.divisor_sum(n) + "\n");
      	sc.close();
    }
    /*
     *  ImplementedInterfaceNames method takes an object and prints the name of the interfaces it implemented
     */
    static void ImplementedInterfaceNames(Object o){
        Class[] theInterfaces = o.getClass().getInterfaces();
        for (int i = 0; i < theInterfaces.length; i++){
            String interfaceName = theInterfaces[i].getName();
            System.out.println(interfaceName);
        }
    }
}
class MyCalculator implements AdvancedArithmetic {
    public int divisor_sum(int n) {
        if (n <= 1) { return n; }

        int res = n + 1;
        for (int i = 2; i < n; i++) {
            if (n % i == 0) {
                res += i;
            }
        }

        return res;
    }
}

<!-- question five: Method Overriding I -->
import java.util.*;
class Sports{

   String get_name()
   {
      return "Generic Sports";
   }
   void get_number_of_team_members()
   {
      System.out.println("Each team has n players in "+get_name());
   }
}

class Soccer extends Sports
{
   String get_name()
   {
      return "Soccer Class";
   }
   //Complete the code
    void get_number_of_team_members(){
        System.out.println("Each team has 11 players in Soccer Class");
    }
}
public class Main
{
   
   public static void main(String []args)
   {
      Sports C1=new Sports();
      Soccer C2=new Soccer();
      System.out.println(C1.get_name());
      C1.get_number_of_team_members();
      System.out.println(C2.get_name());
      C2.get_number_of_team_members();
   }
}

<!-- question six: Java Method Overriding 2 (Super Keyword)

 -->
 import java.util.*;
import java.io.*;


class BiCycle
{
   String define_me()
   {
      return "a vehicel with pedals.";
   }
}

class MotorCycle extends BiCycle
{
   String define_me()
   {
      return "a cycle with an engine.";
   }
   
   MotorCycle()
   {
      
      
      System.out.println("Hello I am a motorcycle, I am "+ define_me());
      String temp=super.define_me();
      System.out.println("My ancestor is a cycle who is "+ temp );
   }
   
}
class Solution{
   public static void main(String []argh)
   {
      MotorCycle M=new MotorCycle();
   }
}

<!-- question seven: Java Instanceof keyword

 -->
 public class InstanceOFTutorial{
	
   static String count(ArrayList mylist){
      int a = 0,b = 0,c = 0;
      for(int i = 0; i < mylist.size(); i++){
         Object element=mylist.get(i);
         if(~~Complete this line~~)
            a++;
         if(~~Complete this line~~)
            b++;
         if(~~Complete this line~~)
            c++;
      }
      String ret = Integer.toString(a)+" "+ Integer.toString(b)+" "+ Integer.toString(c);
      return ret;
   }

   public static void main(String []args){
      ArrayList mylist = new ArrayList();
      Scanner sc = new Scanner(System.in);
      int t = sc.nextInt();
      for(int i=0; i<t; i++){
         String s=sc.next();
         if(s.equals("Student"))mylist.add(new Student());
         if(s.equals("Rockstar"))mylist.add(new Rockstar());
         if(s.equals("Hacker"))mylist.add(new Hacker());
      }
      System.out.println(count(mylist));
   }
}
class Student{}
class Rockstar{   }
class Hacker{}
public class InstanceOFTutorial{
	
   static String count(ArrayList mylist){
      int a = 0,b = 0,c = 0;
      for(int i = 0; i < mylist.size(); i++){
         Object element=mylist.get(i);
         if(element instanceof Student)
            a++;
         if(element instanceof Rockstar)
            b++;
         if(element instanceof Hacker)
            c++;
      }
      String ret = Integer.toString(a)+" "+ Integer.toString(b)+" "+ Integer.toString(c);
      return ret;
   }

   public static void main(String []args){
      ArrayList mylist = new ArrayList();
      Scanner sc = new Scanner(System.in);
      int t = sc.nextInt();
      for(int i=0; i<t; i++){
         String s=sc.next();
         if(s.equals("Student"))mylist.add(new Student());
         if(s.equals("Rockstar"))mylist.add(new Rockstar());
         if(s.equals("Hacker"))mylist.add(new Hacker());
      }
      System.out.println(count(mylist));
   }
}
