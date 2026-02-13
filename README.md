abstract class demo
{
    public int a;
    demo()
    {
        a = 10;
    }

    abstract public void set();
    
    abstract final public void get();

}

class Test extends demo
{

    public void set(int a)
    {
        this.a = a;
    }

    final public void get()
    {
        System.out.println("a = " + a);
    }

    public static void main(String[] args)
    {
        Test obj = new Test();
        obj.set(20);
        obj.get();
    }
}


20 10 error.
Incorrect Answer!

Explanation

In Java, an abstract method cannot be declared as final because final methods cannot be overridden, whereas abstract methods must be overridden by subclasses.
In the program, the method abstract final public void get(); in the demo class causes a compilation error since it violates this rule.
_----_-----------------------------
How can you correctly initialize a 2D array in Java?

A
int[][] arr = new int(3,3);

B
int arr[][] = {{1,2}, {3,4}};

C
int arr[][] = new int[2][2]{{1,2}, {3,4}};

D
int arr[2][2] = {1,2,3,4};

Incorrect Answer!

Explanation

Option B is correct because Java allows initialization using nested braces {}.

---------------------------
What will be the output of this program?


class Demo {
    int num;
    Demo() {
        this(100);
        System.out.println("Default Constructor");
    }
    Demo(int n) {
        num = n;
        System.out.println("Parameterized Constructor");
    }
}
public class Main {
    public static void main(String[] args) {
        Demo obj = new Demo();
    }
}


A
Default Constructor

B
Parameterized Constructor

C
Parameterized Constructor
Default Constructor

D
Compilation Error...

-------------------------
How can one constructor call another constructor within the same class?

A
Using super()

B
Using this()

C
Using new()

D
Constructors cannot call each other



Incorrect Answer!

Explanation

In Java, this() is used to call another constructor of the same class, allowing constructor chaining.

',,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,
Static vs Instance Block Order
Java
Copy code
class Test {
    static { System.out.print("A"); }
    { System.out.print("B"); }

    Test() { System.out.print("C"); }

    public static void main(String[] args) {
        new Test();
        new Test();
    }
}
Options:
A. ABCBC
B. ABCC
C. ACBBC
D. Compilation Error
Answer: A — ABCBC
Flow: Static → Instance → Constructor → Instance → Constructor.

Wrapper Comparison Edge
Java
Copy code
public class Test {
    public static void main(String[] args) {
        Integer a = 128;
        Integer b = 128;
        System.out.println(a == b);
    }
}
Answer: false
Reason: Cache range is -128 to 127.

. 6. Exception + Return in Finally
Java
Copy code
public class Test {
    static int test() {
        try {
            return 1;
        } finally {
            return 2;
        }
    }

    public static void main(String[] args) {
        System.out.println(test()); ki
    }
}
Answer: 2
Reason: finally overrides return.

__________
12. Interface Static Method
Java
Copy code
interface A {
    static void show() { System.out.println("A"); }
}

class Test implements A {
    public static void main(String[] args) {
        show();
    }
}
Answer: Compilation Error
Why: Must call A.show().
