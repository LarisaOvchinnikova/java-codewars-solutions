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

* [x] Count words that doesn't contains letter 'e' (Homework)
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
```
* [x] [1/n- Cycle](https://www.codewars.com/kata/1-slash-n-cycle/train/java)
> Let be n an integer prime with 10 e.g. 7.
    1/7 = 0.142857 142857 142857 ....
    We see that the decimal part has a cycle: 142857. The length of this cycle is 6. In the same way:
    1/11 = 0.09 09 09 .... Cycle length is 2.
    Task:  Given an integer n (n > 1), the function cycle(n) returns the length of the cycle if n and 10 are coprimes, otherwise returns -1.
```java
class Cycle {
    public static int cycle(int n) {
        if (n % 2 == 0 || n % 5 == 0) return -1;
        int d = 9;
        int k = 1;
        while (d % n > 0) {
           d = (d % n) * 10 + 9;
           k++;
        }
        return k;
    }
}
```
* [x] [Training JS #7: if..else and ternary operator](https://www.codewars.com/kata/57202aefe8d6c514300001fd/solutions/java)
> Complete function saleHotdogs/SaleHotDogs, function accept 1 parameters:n, n is the number of customers to buy hotdogs, different numbers have different prices (refer to the following table), return a number that the customer need to pay how much money.
 ```java
 public class SaleHotdogs{
   public static int saleHotdogs(final int n){
    return (n < 5) ? 100 * n : (n < 10) ? 95 * n : 90 * n;
   }
 }
 ```
* [x] [Square(n) Sum](https://www.codewars.com/kata/square-n-sum/train/java/5d39348b707f1e00219ab985) 
> Complete the square sum function so that it squares each number passed into it and then sums the results together.

```java 
 public class Kata
  {
   public static int squareSum(int[] n)
   { 
    int sum = 0;
    for (int i = 0; i < n.length; i++){
      sum += n[i] * n[i];
    }
    return sum;
   }
  }
```
* [x] [Playing with cubes I](https://www.codewars.com/kata/playing-with-cubes-i/train/java)
> Create a public class called Cube without a constructor which gets one single private Integer variable Side, a getter GetSide() and a setter SetSide(int num) method for this property. Actually, getter and setter methods are not the common way to write this code in C#. In the next kata of this series, we gonna refactor the code and make it a bit more professional... Note: There's no need to check for negative values!
```java
public class Cube {
   int Side;
    int getSide(){
       return Side;
    }
    public void setSide(int Side){
        this.Side = Side;
    }
}

---
public class Main {
  public static void main(String... args) {
    Cube c = new Cube();
    c.setSide(5);
    System.out.println(c.getSide());
  }
}

```
* [x] [Is n divisible by x and y?](https://www.codewars.com/kata/is-n-divisible-by-x-and-y/train/java)
> Create a function isDivisible(n, x, y) that checks if a number n is divisible by two numbers x AND y. All inputs are positive, non-zero digits.
```java
public class DivisibleNb {
	public static boolean isDivisible(long n, long x, long y) {
		return (n % x == 0 & n % y == 0);
	}
}
```
* [x] [Reversed Words](https://www.codewars.com/kata/51c8991dee245d7ddf00000e/train/java)
> Complete the solution so that it reverses all of the words within the string passed in.
```java
public class ReverseWords{
 public static String reverseWords(String str){
    String[] words = str.split("\\s");
    String s = "";
    for (int i = words.length - 1; i >= 0; i--){
      s = s + words[i] + ' ';
    }
    return s.trim();
 }
}
```
* [x][8kyu interpreters: HQ9+](https://www.codewars.com/kata/8kyu-interpreters-hq9-plus/train/java)
> You task is to implement an simple interpreter for the notorious esoteric language HQ9+ that will work for a single character input:
  If the input is 'H', return 'Hello World!'
  If the input is 'Q', return the input
  If the input is '9', return the full lyrics of 99 Bottles of Beer.
```java
public class HQ {
  public static String HQ9(char code) {
  String s = "";
  if (code == 'H') return "Hello World!";
  else
  if (code == 'Q') return "Q";
  else
  if (code == '9') {
   for (int i = 99; i >=3; i--){
     s = s + i+" bottles of beer on the wall, "+ i+" bottles of beer.\nTake one down and pass it around, "+ (i-1)+" bottles of beer on the wall.\n";
   }
   s = s +"2 bottles of beer on the wall, 2 bottles of beer.\nTake one down and pass it around, 1 bottle of beer on the wall.\n1 bottle of beer on the wall, 1 bottle of beer.\nTake one down and pass it around, no more bottles of beer on the wall.\nNo more bottles of beer on the wall, no more bottles of beer.\nGo to the store and buy some more, 99 bottles of beer on the wall.";
   return s;
   }
   else return null;
  }
}
```
* [x] [Maximum Multiple](https://www.codewars.com/kata/maximum-multiple/train/java)
> Given a Divisor and a Bound , Find the largest integer N , Such That ,
  
  Conditions :
  N is divisible by divisor
  
  N is less than or equal to bound
  
  N is greater than 0.
```java
public class MaxMultiple {
  public static int maxMultiple(int divisor, int bound) {
    int res = 0;
    if (bound < divisor) res = 0;
      for (int i = bound; i > 0; i--){
       if (i % divisor == 0) {res = i; break;}
      }
      return res;
  }
}
```
* [x] [Lombok Encapsulation](https://www.codewars.com/kata/lombok-encapsulation/train/java)
```java
public class EncapsulationDemo{
  private int number;
  private String stringValue;
  private Object anObject;
  
  int getNumber (){
    return number;
  }
  public void setNumber (int number) {
    this.number = number;
  }
  
  String getStringValue (){
    return stringValue;
  }
  public void setStringValue (String stringValue) {
    this.stringValue = stringValue;
  }
 
  Object getAnObject(){
    return anObject;
  }
  public void setAnObject (Object anObject) {
    this.anObject = anObject;
  }
 
  public EncapsulationDemo() { }

  public EncapsulationDemo(int number, String stringValue, Object anObject){
    this.number = number;
    this.stringValue = stringValue;
    this.anObject = anObject;
  }
}
```
* [x] [Building blocks](https://www.codewars.com/kata/building-blocks/train/java)
> Write a class Block that creates a block (Duh..)
  The constructor should take an array as an argument, this will contain 3 integers of the form [width, length, height] from which the Block should be created.
```java
public class Block{
  private int[]block;

 public Block(int[]block){
   this.block = block;
}
 
 int getWidth(){
    return block[0];
 }
 int getLength(){
    return block[1];
 }
 int getHeight(){
    return block[2];
 } 

 int getVolume(){
   return block[0] * block[1] * block[2];
 }
 int getSurfaceArea(){
   return 2 * (block[0] * block[1] + block[0] * block[2] + block[1] * block[2]);
 }
}
```  
  