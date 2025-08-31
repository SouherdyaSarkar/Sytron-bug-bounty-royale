# Bug Bounty Royale – Final (Java)

Below are 5 codeblocks. Each contains hidden bugs.  
Your task:  
1. Identify and fix the bug(s).  
2. Run the corrected code.  
3. Submit the **final correct output**.  

## Q1. Fix the code to provide the expected output - 

```
1 2 4 8 16
```

```java
public class Test1 {
    public static void main(String[] args) {
        int[] arr = new int[5];
        arr[0] = 1;
        for(int i=1; i<=arr.length; i++) {
            arr[i] = arr[i-1] * 2;
        }
        for(int i=0; i<arr.length; i++);
            System.out.print(arr[i] + " ");
    }
}
```

## Q2. Fix the code to provide the expected output - 

```
5 10 15 20
```

```java
public class Test2 {
    public static void main(String[] args) {
        int[][] matrix = {{5,10},{15,20}};
        for(int i=0; i<=matrix.length; i++) {
            for(int j=0; j<=matrix[i].length; j++) {
                System.out.print(matrix[i][j] + " ");
            }
        }
    }
}
```

## Q3. Fix the code to provide the expected output - 

```
5.5
```

```java
public class Test3 {
    public static void main(String[] args) {
        int a = 11;
        int b = 2;
        double c = a / b;
        System.out.println(c);
    }
}
```

## Q4. Fix the code to provide the expected output - 

```
28
```

```java
public class Test8 {
    public static void main(String[] args) {
        int a = 5;
        int b = 10;
        int c = a++ + ++b + b--;
        System.out.println(c);
    }
}
```

## Q5. Fix the code to provide the expected output - 

```
HelloJava
```

```java
public class Test5 {
    public static void main(String[] args) {
        String s1 = "Hello";
        String s2 = new String("Java");
        if(s1 + s2 == "HelloJava") {
            System.out.println("HelloJava");
        } else {
            System.out.println(s1.concat(s2));
        }
    }
}
```

