# CS-23.202
[Program 1: WAP for 1D array](#assignment-1)


[Program 2: WAP for 2D array](#assignment-2)


[Program 3:WAP for Distance](#assignment-3)
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
