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