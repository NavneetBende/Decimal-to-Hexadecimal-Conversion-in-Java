# Decimal-to-Hexadecimal-Conversion-in-Java
Decimal to Hexadecimal Conversion
On this page we will learn to the logic to convert Decimal to Hexadecimal. And then learn to create Java program for Decimal to Hexadecimal Conversion.

java program to convert decimal to hexadecimal
Method 1
To know how to solve this you must first have knowledge of ASCII Table. The program works in two cases

If the current remainder left >= 10
Must be replaced by (A – F)
Else if current remainder < 10
Must be replaced by (0- 9)
Decimal to Hexadecimal in Java
Related Pages
Decimal to Binary conversion

Decimal to Octal Conversion

Decimal to Hexadecimal Conversion

Binary to Octal conversion

Octal to Binary conversion

Quadrants in which a given coordinate lies

Java Code
Run
 public class Main 
{
  
 
 
public static void main (String[]args) 
  {
    
 
 
int decimal = 1457;
    
 
 
convert (decimal);
  
 
 
} 
 
static void convert (int num) 
  {
    
 
 
			// creating a char array to store hexadecimal equivalent
    char[] hexa = new char[100];
    
 
      // using i to store hexadecimal bit at given array position
    int i = 0;
    
while (num != 0)
      
      {
    
int rem = 0;
  
 
 
rem = num % 16;
   
 
       // check if rem < 10 : Digits : 0 - 9
          // ascii 0 : 48
        if (rem < 10)
          {
        hexa[i] = (char) (rem + 48);
           i++;
         }                    
         // else positional values : A - F 
         // rem value will be > 10, adding 55 will result : A - F 
        // ascii A : 65, B : 66 ..... F : 70 
      else
     
       {
        
hexa[i] = (char) (rem + 55);
          
i++;
        
} 
num = num / 16;
      
} 
// printing hexadecimal array in reverse order
      System.out.println ("Hexadecimal:");
    
for (int j = i - 1; j >= 0; j--)
      
System.out.print (hexa[j]);

} 
 
} 
Output
Hexadecimal : 5B1
