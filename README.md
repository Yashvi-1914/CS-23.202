# CS-23.202
[Program 1: WAP for 1D array](#assignment-1)


[Program 2: WAP for 2D array](#assignment-2)
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
