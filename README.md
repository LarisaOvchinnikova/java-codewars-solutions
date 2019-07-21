## My first steps in Java

Tasks list

* [x] [Beginner - Lost Without a Map](https://www.codewars.com/kata/beginner-lost-without-a-map/train/java/5d279e31c1e94c000f8520f5)
> Given an array of integers, return a new array with each value doubled.
```java
public class Maps {
  public static int[] map(int[] arr) {
   for (int i = 0; i <arr.length; i++){
      arr[i] *=2;
   }
   return arr;
  }
}
```

* [x] [Multiply](https://www.codewars.com/kata/multiply/train/java/5d271474c1e94c00297de6bc)
> The code does not execute properly. Try to figure out why.
```java
public class Multiply {
    public static Double multiply(Double a, Double b) {
        return a * b;
    }
}
```
* [x] [Surface Area and Volume of a Box](https://www.codewars.com/kata/surface-area-and-volume-of-a-box/train/java)
> Write a function that returns the total surface area and volume of a box as an array: [area, volume]
```java
public class Kata {
    public static int[] getSize(int w,int h,int d) {
       int s = 2 * (w*h + w*d + h*d);
       int v = w * h * d;
       return new int [] {s, v};
    }
}
```

* [x] [Is it even?](https://www.codewars.com/kata/is-it-even/train/java)
> Your code will determine if the number passed is even (or not).
```java 
public class Number {
  public boolean isEven(double n) {
      if ( n % 2 == 0) {
      return true;
      } else {
      return false;
      }
  }
}
```

* [x] Task from Interview 
> Find sum of two largest elements in array using one loop
```java
public class Main {
    public static void main(String[] args) {
        int [] a = {1, 7, 5, 2, 8, 4};
        int maxB = a[0];
        int maxS = a[1];
        int temp;
        for  (int i = 1; i < a.length; i++){
            if (a[i] > maxB) {
                temp = maxB;
                maxB = a[i];
                maxS = temp;
            }
        }
        System.out.println(maxB);
        System.out.println(maxS);
        int sum = maxB + maxS;
        System.out.println(sum);
    }
}
```
* [x] [Maximum Product](https://www.codewars.com/kata/maximum-product/train/java)
> Given an array of integers. Find the maximum product obtained from multiplying 2 adjacent numbers in the array.
```java
public class MaxProduct {
  public int adjacentElementsProduct(int[] arr) {
    // your code here
   int max = arr[0] * arr[1];
   for (int i = 0; i < arr.length-1; i++){
     if (arr[i] * arr[i+1] > max) {
        max = arr[i] * arr[i+1];}
   }
   return max;
  }
}
```
* [x] Count of letters 'e' in array
```java
public class Main {
    public static void main(String[] args) {
        String[][] arr = {{"Привет", "всем", "кто"}, {"изучает", "язык", "пограммирования", "java"}};
        int n = 0;
        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < arr[i].length; j++){
                for (int k = 0; k < arr[i][j].length(); k++) {
                    if (arr[i][j].charAt(k) == 'е') {
                        n++;
                    }
                }
            }
        }
        System.out.println(n);
    }
}
```

* [x] Count words that doesn't contains letter 'e'
```java
public class Main {

    public static void main(String[] args) {

        String[][] arr = {{"Привет", "всем", "кто"}, {"изучает", "язык", "пограммирования", "java"}};
        int n = 0;
        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < arr[i].length; j++){
                if (!arr[i][j].contains("е")) {
                  n++;
               }

            }
        }
}
