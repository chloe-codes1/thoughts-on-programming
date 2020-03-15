# Does Java pass by reference or pass by value

> Will cover one of the biggest confusion in Java programming language is whether Java is Pass by Value or Pass by Reference.

<br><br>

Many programming languages allow passing parameters by reference or by value. 

In Java, **we can only pass parameters by value**.

<br>

ex)

```java
package test01;

public class Pass_by_value {
	public static void main(String[] args) {
		Breakfast toast = new Breakfast("toast");
		Breakfast bagel = new Breakfast("bagle");
		
		swap(toast,bagel);
		System.out.println("should be bagel after swapped  => "+ toast.getMenu());
        //should be bagel after swapped  => toast
		System.out.println("should be toast after swapped  => "+ bagel.getMenu());
        //should be toast after swapped  => bagle
	}
	
	public static void swap(Object a, Object b) {
		Object temp = a;
		a = b;
		b = temp;
	}
}

class Breakfast{
	private String menu;

	public Breakfast() {}
	
	public Breakfast(String menu) {
		this.menu = menu;
	}
	public String getMenu() {
		return menu;
	}
	public void setMenu(String menu) {
		this.menu = menu;
	}
}
```

<br>

- `swap()` method did not worked since Java is **pass by value**
- When we use **new** operator to create an instance of a class, the instance is created and the variable contains the reference location of the memory where the object is saved
  - let’s assume that “toast” is pointing to 50 and “bagel” is pointing to 100 and these are the memory location of both Breakfast objects.
- when we are calling swap() method, two new variables `a` and `b` are created pointing to 50 and 100 respectively.
- Notice that we are changing values of `a` and `b` but they are copies of “toast” and “bagel” reference locations, so actually there is no change in the values of “bagel” and “toast” and hence the output.

<br>