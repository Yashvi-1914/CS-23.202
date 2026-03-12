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






    
   
        






