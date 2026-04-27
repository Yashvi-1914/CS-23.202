# CS-23.202
[Program 1: WAP for 1D array](#assignment-1)


[Program 2: WAP for 2D array](#assignment-2)


[Program 3:WAP for Distance](#assignment-3)


[Program 4:WAP for 4 methods addition, subtracton, multiplication, division and test all the methods in main](#assignment-4)


[Program 5:WAP for the addition of 2 times where each time is given in hrs, mins,secs](#assignment-5)


[Program 6:WAP for addition of 2 Distances where each distance is given in meters and cms](#assignment-6)


[Program 7:WAP for addition of 2 Times where each time is given in hours and minutes](#assignment-7)


[Program 8:WAP to do the reverse of an 1D array with necessary number of methods for number of matrix operations like transpose, addition, multiplication, sum of rows, sum of columns, sum of diagonal](#assignment-8)


[Program 9:Collect any 5 codes in c language like factorial,fabonnaci series, armstrong number , swapping of 2 numbers, pattern of stars. convert it in java object oriented language and test it in main](#assignment-9)


[Program 10:Demonstration of dynamic method dispatch](#assignment-10)


[Program 11:WAP using three different classes and methods and print 1-100 three times with thread](#assignment-11)


 [Program 12:Write the program 11 without thread and analyse the result and repeat the same program using runnable interface](#assignment-12)
 

[Program 13:WAP to copy a file using character stream](#assignment-13)


[Program 14:WAP to copy a file using byte stream](#assignment-14)


[Program 15:Write a Java program to demonstrate the use of ArrayList by performing operations such as adding elements, removing elements, searching for an element, updating elements, and iterating through the list.](#assignment-15)


[Program 16:Write a Java program to implement LinkedList and perform insertion at the beginning, middle, and end, along with deletion, searching, and displaying the elements.](#assignment-16)


[Program 17:Write a Java program to demonstrate Stack operations using the Collection Framework, including push, pop, peek, and checking whether the stack is empty.](#assignment-17)


[Program 18:Write a Java program to implement HashMap and perform operations such as inserting key-value pairs, retrieving values using keys, removing entries, and iterating through the map.](#assignment-18)


[Program 19:Write a Java program to demonstrate TreeMap by inserting elements, displaying them in sorted order, searching for a key, and removing elements.](#assignment-19)



[Program 20:Implement a Java class Division with methods for integer division, floating-point division, division with remainder, and dividing multiple numbers by a given divisor. Ensure division by zero is properly handled with exceptions.](#assignment-20)


[Program 21:


## assignment-1
```
import java.util.Scanner;
public class ArrayTest {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        arr a1=new arr();
        a1.input();
        a1.output1();
        a1.rev();
    }
    
}
class arr{
    int x[];
    int rev[];
    
    void input(){
        x = new int[5];
        System.out.println("Enter the elements of array:");
        Scanner sc = new Scanner(System.in);
        for(int i=0;i<5;i++){
           x[i] = sc.nextInt(); 
        }
    }
    void output1(){
        for(int j=0;j<5;j++){
        System.out.println(x[j]);
        }
    }
    void rev(){
        rev = new int[5];
        for(int j=0;j<5;j++){
            rev[4-j] = x[j];
        }
        for(int j=0;j<5;j++){
        System.out.println(rev[j]);
        }
    }
    
}
```


<img width="1205" height="275" alt="image" src="https://github.com/user-attachments/assets/337dbfc9-d6b6-41c9-9866-6daad1298b6b" />


## assignment-2
```
import java.util.Scanner;
public class Array_test {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        test t1= new test();
        t1.input();
        System.out.println("Original Array:");
        t1.outputarr();
        t1.input();
        System.out.println("Reversed Array:");
        t1.outputrev();
    }
    
}
class test{
    int arr[][];
    int rev[][];
    
    void input()
    {
        arr = new int[5][5];
        Scanner sc = new Scanner(System.in); 
        for(int i=0; i<5;i++){
            System.out.println("Enter next:");
            arr[i][i]=sc.nextInt();
        }
    }
    
    void outputarr(){
        for(int i=0;i<5;i++){
            System.out.println(arr[i][i]);
        }
    }
    void outputrev(){
        for(int i=0;i<5;i++){
            System.out.println(rev[i][i]);
        }
    }
    void rev(){
        for(int i =0;i<5;i++){
            rev[i][i]=arr[i][i];
        }
    }
}

```
<img width="1166" height="229" alt="image" src="https://github.com/user-attachments/assets/fedd43a7-3844-4c76-96a3-5ba75a9e3bfe" />

    }
    
}
## assignment-3
```
import java.util.Scanner;
public class DisTest {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
       Distance D1= new Distance();
       Distance D2= new Distance();
       Distance D3= new Distance();
       
       System.out.println("Enter first distance:");
       D1.input();
       System.out.println("Enter second distance:");
       D2.input();
       D3.add(D1,D2);
       System.out.println("Result:");
       D3.output();
       
      
    }
    
}
class Distance{
    int mtr;
    int cm;
    int mm;
    
    void input(){
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter the value of mtr");
        mtr= sc.nextInt();
        System.out.println("Enter the value of cm");
        cm= sc.nextInt();
        System.out.println("Enter the value of mm");
        mm= sc.nextInt();
    }
    
    void output(){
        System.out.println("Meters:" +mtr);
        System.out.println("Centimeters:" +cm);
        System.out.println("Millimeters:" +mm);
    }
    
    void add(Distance O1, Distance O2){
        this.mtr = O1.mtr + O2.mtr +(this.cm/100);
        this.cm = O1.cm + O2.cm;
        this.mm = O1.mm + O2.mm;
        this.mm = this.mm % 10;
        this.cm = this.cm % 100;
    }
}

```
<img width="1184" height="230" alt="image" src="https://github.com/user-attachments/assets/422856ac-1dd0-4ecd-b495-4df1bf2a2d7c" />

## assignment-4

```

import java.util.Scanner;
public class FourMethods {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter first number:");
        int a = sc.nextInt();
        System.out.println("Enter second number:");
        int b = sc.nextInt();
        
        Operations obj = new Operations();
        obj.addition(a,b);
        obj.subtraction(a,b);
        obj.multiplication(a,b);
        obj.division(a,b);
        
     
    }
    
}

class Operations{
    int a;
    int b;
    
    void addition(){
        System.out.println("Addition = " + (a+b));
    }
    
    void subtraction(){
        System.out.println("Subtraction = "+ (a-b));
    }
    
    void multiplication(){
        System.out.println("Multiplication = " +(a*b));
    }
    
    void division(){
        System.out.println("Division = " +(a/b));
    }
}

```
<img width="1266" height="274" alt="image" src="https://github.com/user-attachments/assets/27baeed3-18f9-45f3-a963-8b2ac691ba76" />

## assignment-5

```
import java.util.Scanner;
public class TimeAddition {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter first time(hrs min sec):");
      int h1 = sc.nextInt();
      int m1 = sc.nextInt();
      int s1 = sc.nextInt();
      System.out.println("Enter second time(hrs min sec):");
      int h2 = sc.nextInt();
      int m2 = sc.nextInt();
      int s2 = sc.nextInt();
      Time t = new Time();
      t.add(h1,m1,s1,h2,m2.s2);
    }
    
}

class Time{
    int hrs;
    int min;
    int sec;
    
    void add(int h1,int m1,int s1,int h2,int m2,int s2){
        sec = s1 + s2;
        min = m1 + m2;
        hrs = h1 + h2;
        
        if (sec >=60){
            sec = sec - 60;
            hrs = hrs + 1;
        }
        
        if (min >=60){
            min = min - 60;
            hrs = hrs + 1;
        }
         System.out.println("Sum of Time = " +hrs +"hrs" +min +"min" +sec +"sec");
    }
}

```
<img width="1279" height="310" alt="image" src="https://github.com/user-attachments/assets/689956d4-ea6d-419d-aa78-df260902d888" />

## assignment-6

```

import java.util.Scanner;
public class DistanceAddition {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Distance d1 = new Distance();
        Distance d2 = new Distance();

        System.out.println("Enter first distance:");
        d1.input(sc);

        System.out.println("Enter second distance:");
        d2.input(sc);

        Distance sum = d1.add(d2);

        System.out.print("Total Distance = ");
        sum.display();

        sc.close();
    }
}
    }
    
}
class Distance {
    int meter;
    int cm;

    void input(Scanner sc) {
        System.out.print("Enter meter: ");
        meter = sc.nextInt();

        System.out.print("Enter cm: ");
        cm = sc.nextInt();
    }

    Distance add(Distance d) {
        Distance result = new Distance();

        result.cm = this.cm + d.cm;
        result.meter = this.meter + d.meter;

        // convert cm to meter if >= 100
        if (result.cm >= 100) {
            result.meter += result.cm / 100;
            result.cm = result.cm % 100;
        }

        return result;
    }

    void display() {
        System.out.println(meter + " meter " + cm + " cm");
    }
}

```
<img width="1265" height="278" alt="image" src="https://github.com/user-attachments/assets/b5f4dcb8-5a41-4831-b06a-6b6f77908e01" />

## assignment-7

```

import java.util.Scanner;
public class timeadd {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
      Scanner sc = new Scanner(System.in);

        Time t1 = new Time();
        Time t2 = new Time();

        System.out.println("Enter first time:");
        t1.input(sc);

        System.out.println("Enter second time:");
        t2.input(sc);

        Time sum = t1.add(t2);

        System.out.print("Total Time = ");
        sum.display();

        sc.close();
    }
}
  
    


class Time {
    int hrs;
    int mins;

    void input(Scanner sc) {
        System.out.print("Enter hours: ");
        hrs = sc.nextInt();

        System.out.print("Enter minutes: ");
        mins = sc.nextInt();
    }

    Time add(Time t) {
        Time result = new Time();

        result.hrs = this.hrs + t.hrs;
        result.mins = this.mins + t.mins;

        // Convert minutes to hours if >= 60
        if (result.mins >= 60) {
            result.hrs += result.mins / 60;
            result.mins = result.mins % 60;
        }

        return result;
    }

    void display() {
        System.out.println(hrs + " hours " + mins + " minutes");
    }
}

```
<img width="1264" height="282" alt="image" src="https://github.com/user-attachments/assets/0168fa16-df13-4b84-b117-985fae196587" />

## assignment-8

```

import java.util.Scanner;
public class MatrixMain {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
       Scanner sc = new Scanner(System.in);
        MatrixOperations obj = new MatrixOperations();

        // 1D Array Reverse
        System.out.print("Enter size of array: ");
        int n = sc.nextInt();

        int arr[] = new int[n];

        System.out.println("Enter array elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        obj.reverseArray(arr, n);

        // Matrix Input
        System.out.print("Enter rows and columns: ");
        int r = sc.nextInt();
        int c = sc.nextInt();

        int a[][] = new int[r][c];
        int b[][] = new int[r][c];

        System.out.println("Enter first matrix:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                a[i][j] = sc.nextInt();
            }
        }

        System.out.println("Enter second matrix:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                b[i][j] = sc.nextInt();
            }
        }

        obj.addMatrix(a, b, r, c);
        obj.transpose(a, r, c);
        obj.multiplyMatrix(a, b, r, c);
        obj.sumRows(a, r, c);
        obj.sumColumns(a, r, c);

        if (r == c) {
            obj.sumDiagonal(a, r);
        } else {
            System.out.println("Diagonal sum only for square matrix.");
        }

        sc.close();
    }
}
    
    

class MatrixOperations {

    // Reverse 1D Array
    public void reverseArray(int arr[], int n) {
        System.out.println("Reversed Array:");
        for (int i = n - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

    // Matrix Addition
    public void addMatrix(int a[][], int b[][], int r, int c) {
        int sum[][] = new int[r][c];

        System.out.println("Matrix Addition:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                sum[i][j] = a[i][j] + b[i][j];
                System.out.print(sum[i][j] + " ");
            }
            System.out.println();
        }
    }

    // Matrix Transpose
    public void transpose(int a[][], int r, int c) {
        System.out.println("Transpose of Matrix:");
        for (int i = 0; i < c; i++) {
            for (int j = 0; j < r; j++) {
                System.out.print(a[j][i] + " ");
            }
            System.out.println();
        }
    }

    // Matrix Multiplication
    public void multiplyMatrix(int a[][], int b[][], int r, int c) {
        int mul[][] = new int[r][c];

        System.out.println("Matrix Multiplication:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                mul[i][j] = 0;
                for (int k = 0; k < c; k++) {
                    mul[i][j] += a[i][k] * b[k][j];
                }
                System.out.print(mul[i][j] + " ");
            }
            System.out.println();
        }
    }

    // Sum of Rows
    public void sumRows(int a[][], int r, int c) {
        System.out.println("Sum of Rows:");
        for (int i = 0; i < r; i++) {
            int sum = 0;
            for (int j = 0; j < c; j++) {
                sum += a[i][j];
            }
            System.out.println("Row " + (i + 1) + " = " + sum);
        }
    }

    // Sum of Columns
    public void sumColumns(int a[][], int r, int c) {
        System.out.println("Sum of Columns:");
        for (int i = 0; i < c; i++) {
            int sum = 0;
            for (int j = 0; j < r; j++) {
                sum += a[j][i];
            }
            System.out.println("Column " + (i + 1) + " = " + sum);
        }
    }

    // Sum of Diagonal
    public void sumDiagonal(int a[][], int n) {
        int sum = 0;
        for (int i = 0; i < n; i++) {
            sum += a[i][i];
        }
        System.out.println("Sum of Diagonal = " + sum);
    }
}

```
<img width="1280" height="282" alt="image" src="https://github.com/user-attachments/assets/d1290503-1eec-4db0-9bad-c0952ee7f189" />

## assignment-9

```

import java.util.Scanner;
public class MainProgram {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        BasicPrograms obj = new BasicPrograms();

        System.out.print("Enter number for factorial: ");
        int n = sc.nextInt();
        obj.factorial(n);

        System.out.print("Enter number of terms for Fibonacci: ");
        int f = sc.nextInt();
        obj.fibonacci(f);

        System.out.print("Enter number to check Armstrong: ");
        int a = sc.nextInt();
        obj.armstrong(a);

        System.out.print("Enter two numbers for swapping: ");
        int x = sc.nextInt();
        int y = sc.nextInt();
        obj.swap(x, y);

        System.out.print("Enter rows for star pattern: ");
        int p = sc.nextInt();
        obj.starPattern(p);

        sc.close();
    }
    
}
class BasicPrograms {

    // Factorial
    public void factorial(int n) {
        int fact = 1;
        for(int i = 1; i <= n; i++) {
            fact = fact * i;
        }
        System.out.println("Factorial = " + fact);
    }

    // Fibonacci Series
    public void fibonacci(int n) {
        int a = 0, b = 1, c;
        System.out.println("Fibonacci Series:");
        for(int i = 1; i <= n; i++) {
            System.out.print(a + " ");
            c = a + b;
            a = b;
            b = c;
        }
        System.out.println();
    }

    // Armstrong Number
    public void armstrong(int num) {
        int temp = num, sum = 0, r;

        while(num > 0) {
            r = num % 10;
            sum = sum + (r * r * r);
            num = num / 10;
        }

        if(sum == temp)
            System.out.println(temp + " is Armstrong Number");
        else
            System.out.println(temp + " is Not Armstrong Number");
    }

    // Swapping Two Numbers
    public void swap(int a, int b) {
        int temp;
        temp = a;
        a = b;
        b = temp;

        System.out.println("After Swapping:");
        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }

    // Star Pattern
    public void starPattern(int n) {
        System.out.println("Star Pattern:");
        for(int i = 1; i <= n; i++) {
            for(int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}

```
<img width="1280" height="288" alt="image" src="https://github.com/user-attachments/assets/b5366150-964f-420b-b4da-92a4d0ba5fc4" />

## assignment-10

```
public class Main
{
	public static void main(String[] args) {
	    
	    Child1 c1 = new Child1();
		Child2 c2 = new Child2();
		
		Parent p;
		p = new Child1();
		p.show();
		p = new Child2();
		p.show();
		
		
		
		c1.show();
		c2.show();
	}
}

class Parent{
    void show(){
        System.out.println("You are in parent class");
    }
}

class Child1 extends Parent{
    void show(){
        System.out.println("You are in child 1");
    }
}

class Child2 extends Parent{
    void show(){
        System.out.println("You are in child 2");
    }
}

```
<img width="1001" height="182" alt="image" src="https://github.com/user-attachments/assets/99c3d752-3537-4735-a177-acb56e174279" />

## assignment-11
```
public class MainClass {
    public static void main(String args[])
    {
        A obj1 =  new A();
        B obj2 = new B();
        C obj3 = new C();
        obj1.fun();
        obj2.fun();
        obj3.fun();
    }
    
}
class A
{
    public void fun()
    {
        for(int i=1;i<=100;i++)
        {
            System.out.println("A" + i);
        }
        System.out.println();
    }
}
class B
{
    public void fun(){
        for(int i=1;i<=100;i++)
        {
            System.out.println("B:" + i);
        }
        System.out.println();
    }
}
class C
{
    public void fun()
    {
        for(int i=1;i<=100;i++)
        {
            System.out.println("C" + i);
        }
        System.out.println();
    }
}

```
<img width="1235" height="829" alt="image" src="https://github.com/user-attachments/assets/7ddb45f6-5b70-42b1-88bd-45fb60c67da8" />
```
public class NewMainClass {
    
    public static void main(String args[])
    {
        AA obj1 =  new AA();
        BB obj2 = new BB();
        CC obj3 = new CC();
        obj1.start();
        obj2.start();
        obj3.start();
    }
    
}
class AA extends Thread
{
    
    public void run()
    {
        for(int i=1;i<=100;i++)
        {
            System.out.println("AA" + i);
        }
        System.out.println();
    }
}
class BB extends Thread
{
   
    public void run()
    {
        for(int i=1;i<=100;i++)
        {
            System.out.println("BB:" + i);
        }
        System.out.println();
    }
}
class CC extends Thread
{
    
    public void run()
    {
        for(int i=1;i<=100;i++)
        {
            System.out.println("CC" + i);
        }
        System.out.println();
    }
}


```
<img width="1244" height="740" alt="image" src="https://github.com/user-attachments/assets/5350bbba-2744-4d84-a95c-739dbe8a5778" />

## assignment-12
```
public class NewMClass {
    
    public static void main(String args[])
    {
        AAA obj1 =  new AAA();
        BBB obj2 = new BBB();
        CCC obj3 = new CCC();
        
        Thread th1 = new Thread(obj1);
        Thread th2 = new Thread(obj2);
        Thread th3 = new Thread(obj3);
        
        th1.start();
        th2.start();
        th3.start();
    }
    
}
class AAA implements Runnable
{
    
    public void run()
    {
        for(int i=1;i<=100;i++)
        {
            System.out.println("AAA" + i);
        }
        System.out.println();
    }
}
class BBB implements Runnable
{
   
    public void run()
    {
        for(int i=1;i<=100;i++)
        {
            System.out.println("BBB:" + i);
        }
        System.out.println();
    }
}
class CCC implements Runnable

{
    
    public void run()
    {
        for(int i=1;i<=100;i++)
        {
            System.out.println("CCC" + i);
        }
        System.out.println();
    }
}

```
<img width="1240" height="677" alt="image" src="https://github.com/user-attachments/assets/aec708e6-47be-4063-9e5e-40ec872273cc" />

## assignment-13
```
import java.io.*;

public class CharFileCopy {
    public static void main(String[] args){
        try{
            FileReader fr = new FileReader("source.txt");
            FileWriter fw = new FileWriter("dest_char.txt");
            int ch;
            while ((ch = fr.read())!=-1){
                fw.write(ch);
            }
            fr.close();
            fw.close();
            System.out.println("File copied using character stream");
        } catch(Exception e){
            System.out.println(e);
        }
    }
}
```
<img width="1231" height="515" alt="image" src="https://github.com/user-attachments/assets/21fac287-9ed5-4b05-8e2c-8f2f983b1025" />


## assignment-14
```
import java.io.*;

public class ByteFileCopy {
    public static void main(String[] args){
        try{
            FileInputStream fis = new FileInputStream("source.txt");
            FileOutputStream fos = new FileOutputStream("dest_byte.txt");
            
            int b;
            while((b = fis.read())!= -1){
                fos.write(b);
            }
            fis.close();
            fos.close();
            
            System.out.println("File copied using byte stream");
        }catch(Exception e){
            System.out.println(e);
        }
    }
}

```

<img width="1234" height="523" alt="image" src="https://github.com/user-attachments/assets/c75671bd-1ad3-45b4-b1ce-d2a0f5811073" />

## assignment-15
```
import java.util.*;
public class ArrayListDemo {
    public static void main(String[] args){
        ArrayList<String>list = new ArrayList<>();
        list.add("Apple");
        list.add("Banana");
        list.add("Mango");
        
        list.add(1,"Orange");
        
        System.out.println("Element at index 2:" +list.get(2));
        
        list.set(0,"Grapes");
        
        list.remove("Banana");
        
        System.out.println("Size: " +list.size());
        
        System.out.println("Contains mango?" +list.contains("Mango"));
        
        System.out.println("List elements:");
        for(String item: list){
            System.out.println(item);
        }
            list.clear();
            System.out.println("Is Empty?" + list.isEmpty());
        
    }
}

```
<img width="1201" height="298" alt="image" src="https://github.com/user-attachments/assets/21a71dd7-b737-4417-ab98-032adb6a7c32" />

## assignment-16
```
import java.util.*;
public class LinkedListExample {
    public static void main(String[] args){
        LinkedList<String>list = new LinkedList<>();
        list.add("Apple");
        list.addFirst("Banana");
        list.addLast("Mango");
        
        System.out.println("First:" + list.getFirst());
        System.out.println("Last:" + list.getLast());
        list.set(1,"Orange");
        list.removeFirst();
        list.removeLast();
        
        System.out.println("Size:" + list.size());
        System.out.println("Elements");
        for(String item: list){
            System.out.println(item);
        }
        System.out.println("Conatins Orange?" +list.contains("Orange"));
        list.clear();
        System.out.println("Is Empty?" +list.isEmpty());
    }
}
```
<img width="1203" height="272" alt="image" src="https://github.com/user-attachments/assets/0c0d5683-5ade-43f1-9576-65fb24a73767" />

## assignment-17
```
import java.util.Stack;
public class Main {
    public static void main(String[] args){
        Stack<Integer>stack = new Stack<>();
        stack.push(10);
        stack.push(20);
        stack.push(30);
        
        System.out.println("Stack:" +stack);
        System.out.println("Top element:" +stack.peek());
        System.out.println("Removed:" +stack.pop());
        System.out.println("Stack after pop:" +stack);
    }
}

```
<img width="1197" height="230" alt="image" src="https://github.com/user-attachments/assets/92890487-8184-40c6-b3f6-0d3dac71e39e" />

## assignment-18
```
import java.util.HashMap;
public class Main2 {
    public static void main(String[] args){
        HashMap<Integer,String>map = new HashMap<>();
        map.put(1,"Apple");
        map.put(2,"Banana");
        map.put(3,"Mango");
        
        System.out.println(map.get(2));
        map.remove(1);
        System.out.println(map.containsKey(3));
    }
}

```
<img width="1162" height="166" alt="image" src="https://github.com/user-attachments/assets/efbada04-4b6f-40ed-b780-bab05070e0c4" />

## assignment-19
```
import java.util.TreeSet;
public class Main3{
    public static void main(String[] args){
        TreeSet<Integer>set = new TreeSet<>();
        set.add(50);
        set.add(10);
        set.add(30);
        set.add(20);
        
        System.out.println("TreeSet:" +set);
        System.out.println("First:" +set.first());
        System.out.println("Last:" +set.last());
        
        System.out.println("Higher than 20:" +set.higher(20));
        set.remove(30);
        System.out.println("After removal:" +set);
    }
}
```
<img width="1196" height="261" alt="image" src="https://github.com/user-attachments/assets/2542d4f9-8677-45aa-9a41-28732bf24335" />

## assignment-20
```
public class Division {

    // Integer Division
    public int divideInt(int a, int b) {
        if (b == 0) {
            throw new ArithmeticException("Cannot divide by zero (integer)");
        }
        return a / b;
    }

    // Floating-point Division
    public double divideDouble(double a, double b) {
        if (b == 0.0) {
            throw new ArithmeticException("Cannot divide by zero (double)");
        }
        return a / b;
    }

    // Division with Remainder
    public int divideWithRemainder(int a, int b) {
        if (b == 0) {
            throw new ArithmeticException("Cannot divide by zero (remainder)");
        }
        return a % b;
    }

    // Divide Multiple Numbers by a Given Divisor
    public double[] divideArray(double[] numbers, double divisor) {
        if (divisor == 0.0) {
            throw new ArithmeticException("Cannot divide by zero (array)");
        }

        double[] result = new double[numbers.length];

        for (int i = 0; i < numbers.length; i++) {
            result[i] = numbers[i] / divisor;
        }

        return result;
    }

    // Main method for testing
    public static void main(String[] args) {
        Division d = new Division();

        try {
            // Integer division
            System.out.println("Integer Division: " + d.divideInt(10, 2));

            // Double division
            System.out.println("Double Division: " + d.divideDouble(10.5, 2.5));

            // Remainder
            System.out.println("Remainder: " + d.divideWithRemainder(10, 3));

            // Array division
            double[] arr = {10, 20, 30};
            double[] result = d.divideArray(arr, 2);

            System.out.print("Array Division: ");
            for (double val : result) {
                System.out.print(val + " ");
            }

        } catch (ArithmeticException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```
<img width="859" height="223" alt="image" src="https://github.com/user-attachments/assets/5eb0e478-60bc-4019-8b2a-130c9b848006" />

## assignment-21

```
import java.awt.Color;
import java.awt.Graphics;

/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/GUIForms/JFrame.java to edit this template
 */

/**
 *
 * @author IBM25
 */
public class NewJFrame extends javax.swing.JFrame {
    
    private static final java.util.logging.Logger logger = java.util.logging.Logger.getLogger(NewJFrame.class.getName());

    Graphics g;
    
    public NewJFrame() {
      
        initComponents();
          g= this.getGraphics();
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jButton1 = new javax.swing.JButton();
        jButton2 = new javax.swing.JButton();
        jButton3 = new javax.swing.JButton();
        jButton4 = new javax.swing.JButton();
        jButton5 = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jButton1.setText("jButton1");
        jButton1.addActionListener(this::jButton1ActionPerformed);

        jButton2.setText("jButton2");
        jButton2.addActionListener(this::jButton2ActionPerformed);

        jButton3.setText("jButton3");
        jButton3.addActionListener(this::jButton3ActionPerformed);

        jButton4.setText("Red");
        jButton4.addActionListener(this::jButton4ActionPerformed);

        jButton5.setText("Pink");
        jButton5.addActionListener(this::jButton5ActionPerformed);

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGap(0, 325, Short.MAX_VALUE)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(jButton1, javax.swing.GroupLayout.Alignment.TRAILING)
                    .addComponent(jButton2, javax.swing.GroupLayout.Alignment.TRAILING)
                    .addComponent(jButton3, javax.swing.GroupLayout.Alignment.TRAILING)
                    .addComponent(jButton4, javax.swing.GroupLayout.Alignment.TRAILING)
                    .addComponent(jButton5, javax.swing.GroupLayout.Alignment.TRAILING)))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                .addComponent(jButton4)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.UNRELATED)
                .addComponent(jButton5)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, 161, Short.MAX_VALUE)
                .addComponent(jButton3)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addComponent(jButton2)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addComponent(jButton1))
        );

        pack();
    }// </editor-fold>                        

    private void jButton3ActionPerformed(java.awt.event.ActionEvent evt) {                                         
    g.drawRect(50, 50, 200, 200);
    }                                        

    private void jButton2ActionPerformed(java.awt.event.ActionEvent evt) {                                         
       g.fillOval(20, 20, 200, 30);
    }                                        

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        g.fillRoundRect(30, 30, 30, 50, 10, 10);
    }                                        

    private void jButton4ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        g.setColor(Color.red);
    }                                        

    private void jButton5ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        g.setColor(Color.pink);
    }                                        

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ReflectiveOperationException | javax.swing.UnsupportedLookAndFeelException ex) {
            logger.log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(() -> new NewJFrame().setVisible(true));
    }

    // Variables declaration - do not modify                     
    private javax.swing.JButton jButton1;
    private javax.swing.JButton jButton2;
    private javax.swing.JButton jButton3;
    private javax.swing.JButton jButton4;
    private javax.swing.JButton jButton5;
    // End of variables declaration                   
}

```
<img width="1280" height="949" alt="image" src="https://github.com/user-attachments/assets/1cbc17e0-9d1f-4d67-acd9-d4f368c01cea" />

## assignment-22
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class SimpleCalculator extends JFrame implements ActionListener {

    JTextField num1Field, num2Field, resultField;
    JButton addBtn, subBtn, mulBtn, divBtn;

    public SimpleCalculator() {
        setTitle("Simple Calculator");
        setSize(350, 250);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new GridLayout(5, 2, 10, 10));

        add(new JLabel("Enter Number 1:"));
        num1Field = new JTextField();
        add(num1Field);

        add(new JLabel("Enter Number 2:"));
        num2Field = new JTextField();
        add(num2Field);

        add(new JLabel("Result:"));
        resultField = new JTextField();
        resultField.setEditable(false);
        add(resultField);

        addBtn = new JButton("Add");
        subBtn = new JButton("Subtract");
        mulBtn = new JButton("Multiply");
        divBtn = new JButton("Divide");

        add(addBtn);
        add(subBtn);
        add(mulBtn);
        add(divBtn);

        addBtn.addActionListener(this);
        subBtn.addActionListener(this);
        mulBtn.addActionListener(this);
        divBtn.addActionListener(this);

        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        try {
            double num1 = Double.parseDouble(num1Field.getText().trim());
            double num2 = Double.parseDouble(num2Field.getText().trim());
            double result = 0;

            if (e.getSource() == addBtn) {
                result = num1 + num2;
            } else if (e.getSource() == subBtn) {
                result = num1 - num2;
            } else if (e.getSource() == mulBtn) {
                result = num1 * num2;
            } else if (e.getSource() == divBtn) {
                if (num2 == 0) {
                    resultField.setText("Cannot divide by zero");
                    return;
                }
                result = num1 / num2;
            }

            resultField.setText(String.format("%.2f", result)); // rounded output

        } catch (NumberFormatException ex) {
            resultField.setText("Invalid input!");
        }
    }

    public static void main(String[] args) {
        new SimpleCalculator();
    }
}
```
<img width="253" height="179" alt="image" src="https://github.com/user-attachments/assets/ad081f39-8f60-420f-86b5-f2ca4ea2bf4b" />

## assignment-23
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class SimplePaint extends JFrame {

    private String currentShape = "Rectangle"; // Default shape
    private Color currentColor = Color.BLACK;  // Default color
    private boolean fillShape = false;         // Default outline only

    public SimplePaint() {
        // Basic Frame Setup
        setTitle("Java Swing Shape Drawer");
        setSize(600, 500);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new BorderLayout());

        // 1. Create the Drawing Canvas
        JPanel canvas = new JPanel() {
            @Override
            protected void paintComponent(Graphics g) {
                super.paintComponent(g);
                g.setColor(currentColor);

                if (currentShape.equals("Rectangle")) {
                    if (fillShape) {
                        g.fillRect(150, 100, 300, 200);
                    } else {
                        g.drawRect(150, 100, 300, 200);
                    }
                } else if (currentShape.equals("Oval")) {
                    if (fillShape) {
                        g.fillOval(150, 100, 300, 200);
                    } else {
                        g.drawOval(150, 100, 300, 200);
                    }
                }
            }
        };
        canvas.setBackground(Color.WHITE);

        // 2. Create the Control Panel (Buttons)
        JPanel controls = new JPanel();
        controls.setLayout(new FlowLayout());

        // Shape Buttons
        JButton rectBtn = new JButton("Rectangle");
        JButton ovalBtn = new JButton("Oval");
        
        // Color Buttons
        JButton redBtn = new JButton("Red");
        JButton blackBtn = new JButton("Black");
        
        // Fill/Outline Toggle
        JButton fillToggle = new JButton("Fill: OFF");

        // 3. Add Action Listeners
        rectBtn.addActionListener(e -> { currentShape = "Rectangle"; canvas.repaint(); });
        ovalBtn.addActionListener(e -> { currentShape = "Oval"; canvas.repaint(); });
        redBtn.addActionListener(e -> { currentColor = Color.RED; canvas.repaint(); });
        blackBtn.addActionListener(e -> { currentColor = Color.BLACK; canvas.repaint(); });
        
        fillToggle.addActionListener(e -> {
            fillShape = !fillShape;
            fillToggle.setText("Fill: " + (fillShape ? "ON" : "OFF"));
            canvas.repaint();
        });

        // Add buttons to the control panel
        controls.add(rectBtn);
        controls.add(ovalBtn);
        controls.add(new JSeparator(JSeparator.VERTICAL));
        controls.add(redBtn);
        controls.add(blackBtn);
        controls.add(fillToggle);

        // Add components to frame
        add(canvas, BorderLayout.CENTER);
        add(controls, BorderLayout.SOUTH);
    }

    public static void main(String[] args) {
        // Run the GUI on the Event Dispatch Thread
        SwingUtilities.invokeLater(() -> {
            new SimplePaint().setVisible(true);
        });
    }
}
```
<img width="436" height="368" alt="image" src="https://github.com/user-attachments/assets/308bc2c3-ebbd-40f0-9ba8-800d4db8df7e" />

## assignment-24
```
import javax.swing.*;
import java.awt.*;
import java.util.Date;
import java.util.Random;

public class MultiFunctionGUI extends JFrame {

    public MultiFunctionGUI() {
        // --- Frame Configuration ---
        setTitle("10-Function Pro GUI");
        setSize(800, 500);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLocationRelativeTo(null); // Center on screen
        setLayout(new BorderLayout(10, 10));

        // Display area for feedback
        JLabel statusLabel = new JLabel("Click a button to interact", SwingConstants.CENTER);
        statusLabel.setFont(new Font("SansSerif", Font.BOLD, 16));
        statusLabel.setBorder(BorderFactory.createEtchedBorder());

        // --- Button Panel (GridLayout: 2 rows, 5 columns) ---
        JPanel buttonPanel = new JPanel(new GridLayout(2, 5, 10, 10));
        buttonPanel.setBorder(BorderFactory.createEmptyBorder(20, 20, 20, 20));

        // 1. Time Display
        JButton btn1 = new JButton("Current Time");
        btn1.addActionListener(e -> statusLabel.setText("Now: " + new Date().toString()));

        // 2. Random Background Color
        JButton btn2 = new JButton("Surprise Color");
        btn2.addActionListener(e -> {
            Random rand = new Random();
            Color randomColor = new Color(rand.nextInt(256), rand.nextInt(256), rand.nextInt(256));
            buttonPanel.setBackground(randomColor);
            statusLabel.setText("Background updated!");
        });

        // 3. Dialog Message
        JButton btn3 = new JButton("Pop-up Alert");
        btn3.addActionListener(e -> JOptionPane.showMessageDialog(this, "This is a Swing Alert!"));

        // 4. Increase Window Size
        JButton btn4 = new JButton("Grow Window");
        btn4.addActionListener(e -> setSize(getWidth() + 20, getHeight() + 20));

        // 5. Input Dialog (Math)
        JButton btn5 = new JButton("Square Root");
        btn5.addActionListener(e -> {
            String input = JOptionPane.showInputDialog("Enter a number:");
            try {
                double val = Double.parseDouble(input);
                statusLabel.setText("√" + val + " = " + Math.sqrt(val));
            } catch (Exception ex) {
                statusLabel.setText("Invalid input!");
            }
        });

        // 6. Toggle Visibility
        JButton btn6 = new JButton("Ghost Button");
        btn6.setToolTipText("I will disappear!");
        btn6.addActionListener(e -> btn6.setVisible(false));

        // 7. Reset UI
        JButton btn7 = new JButton("Reset All");
        btn7.addActionListener(e -> {
            buttonPanel.setBackground(null);
            setSize(800, 500);
            btn6.setVisible(true);
            statusLabel.setText("UI has been reset.");
        });

        // 8. System Properties
        JButton btn8 = new JButton("OS Info");
        btn8.addActionListener(e -> statusLabel.setText("OS: " + System.getProperty("os.name")));

        // 9. Change Font Style
        JButton btn9 = new JButton("Fancy Font");
        btn9.addActionListener(e -> statusLabel.setFont(new Font("Serif", Font.ITALIC | Font.BOLD, 22)));

        // 10. Exit Application
        JButton btn10 = new JButton("Close App");
        btn10.setBackground(new Color(255, 100, 100));
        btn10.addActionListener(e -> System.exit(0));

        // Add all buttons to the grid
        buttonPanel.add(btn1);
        buttonPanel.add(btn2);
        buttonPanel.add(btn3);
        buttonPanel.add(btn4);
        buttonPanel.add(btn5);
        buttonPanel.add(btn6);
        buttonPanel.add(btn7);
        buttonPanel.add(btn8);
        buttonPanel.add(btn9);
        buttonPanel.add(btn10);

        // --- Final Assembly ---
        add(statusLabel, BorderLayout.NORTH);
        add(buttonPanel, BorderLayout.CENTER);
    }

    public static void main(String[] args) {
        // Run in the Event Dispatch Thread (Swing Standard)
        SwingUtilities.invokeLater(() -> {
            new MultiFunctionGUI().setVisible(true);
        });
    }
}
```
<img width="585" height="365" alt="image" src="https://github.com/user-attachments/assets/e1879f9e-a12e-4ced-9437-6b7f81b29e50" />


<img width="584" height="368" alt="image" src="https://github.com/user-attachments/assets/0fdd6b38-215e-4daf-80f4-396647ffb639" />


<img width="584" height="369" alt="image" src="https://github.com/user-attachments/assets/b812a49c-c11f-403b-8105-033847b8c410" />


<img width="602" height="381" alt="image" src="https://github.com/user-attachments/assets/1e58a834-fd9e-4cf5-99b7-af1712a061bc" />


<img width="597" height="380" alt="image" src="https://github.com/user-attachments/assets/9153dac9-2e7b-47f6-a80a-e0e598deb34e" />


<img width="600" height="381" alt="image" src="https://github.com/user-attachments/assets/8b36e5de-9867-4b77-b2ef-0788a21595c9" />


<img width="585" height="367" alt="image" src="https://github.com/user-attachments/assets/f1e3544f-10cc-453c-9c84-802f57843f3f" />


<img width="589" height="368" alt="image" src="https://github.com/user-attachments/assets/c52bf7b3-fa79-4c28-bb3c-8e521c5739c5" />


<img width="589" height="368" alt="image" src="https://github.com/user-attachments/assets/d80edd20-5e48-4580-b20b-054912094439" />

## assignment-25
```
package com.myapp; 

public class Calculator {
    public int add(int a, int b) {
        return a + b;
    }

    public void greetUser(String name) {
        System.out.println("Hello, " + name + "! Welcome to the Package Program.");
    }
}
```
```
import com.myapp.Calculator;

public class Main {
    public static void main(String[] args) {
        // Create an object of the class from the package
        Calculator calc = new Calculator();

        // Use the methods
        calc.greetUser("Developer");
        
        int sum = calc.add(10, 25);
        System.out.println("The result of the package calculation is: " + sum);
    }
}
```
<img width="560" height="94" alt="image" src="https://github.com/user-attachments/assets/ed61db0f-aa92-4230-8ad5-72929b089625" />






















    
   
        






