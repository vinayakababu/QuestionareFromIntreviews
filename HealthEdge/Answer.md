Great set of interview questions, Viyank! Since you’re positioning yourself as a senior backend engineer with strong debugging and escalation-handling experience, I’ll frame the answers in a way that shows both technical depth and practical problem-solving maturity. Let’s go step by step:

---

### 1) What is OOP?
Object-Oriented Programming (OOP) is a paradigm that organizes software design around **objects**—entities that encapsulate **state (fields)** and **behavior (methods)**. Core principles:
- **Encapsulation**: Bundling data and methods together.
- **Abstraction**: Hiding implementation details, exposing only essentials.
- **Inheritance**: Reusing and extending existing classes.
- **Polymorphism**: Allowing different implementations under a common interface.

---

### 2) Is Java 100% OOP?
No. Java is **not 100% OOP** because it supports **primitive data types** (int, char, boolean, etc.) which are not objects. Languages like Smalltalk are closer to 100% OOP.

---

### 3) Difference between Interface vs Abstract Class
| Aspect | Interface | Abstract Class |
|--------|-----------|----------------|
| Methods | Only abstract methods (Java 8+ allows default & static methods) | Can have abstract and concrete methods |
| Variables | Always `public static final` | Can have instance variables |
| Inheritance | A class can implement multiple interfaces | A class can extend only one abstract class |
| Use case | Define contract | Provide partial implementation |

---

### 4) Can we create an object for abstract class?
No, abstract classes cannot be instantiated directly. They must be subclassed, and the subclass can be instantiated.

---

### 5) Does abstract class have a constructor?
Yes. Abstract classes can have constructors, which are called when a subclass object is created.

---

### 6) Access modifiers in Java & role in inheritance/overriding
- **public**: Accessible everywhere.
- **protected**: Accessible within package + subclasses.
- **default (package-private)**: Accessible only within the same package.
- **private**: Accessible only within the class.

**Inheritance/Overriding**:
- Overridden methods cannot reduce visibility (e.g., overriding a `public` method with `protected` is illegal).
- Constructors are not inherited.

---

### 7) Java 8 special methods in interfaces
- **Default methods**: Provide implementation inside interface.
- **Static methods**: Belong to the interface itself, not instances.

---

### 8) Access modifier of variables inside interface
All variables in an interface are implicitly:
- `public static final` (constants).

---

### 9) Approach when a Jira ticket (bug/escalation) is assigned
1. **Understand the issue**: Read description, logs, reproduction steps.
2. **Reproduce**: Try to replicate in dev/staging.
3. **Root cause analysis**: Debug using logs, breakpoints, monitoring tools.
4. **Fix**: Apply minimal-impact solution.
5. **Test**: Unit + regression testing.
6. **Communicate**: Update stakeholders with RCA and resolution.
7. **Prevent recurrence**: Add monitoring, documentation, or code improvements.

---

### 10) Interfaces in Collection Framework
- **Collection**
- **List**
- **Set**
- **Queue**
- **Deque**
- **Map** (though not child of Collection)

---

### 11) Program to identify the biggest palindrome
```java
public class BigPalindrome {
    public static boolean isPalindrome(String str) {
        int i = 0, j = str.length() - 1;
        while (i < j) {
            if (str.charAt(i++) != str.charAt(j--)) return false;
        }
        return true;
    }

    public static void main(String[] args) {
        String[] arr = {"madam", "racecar", "apple", "rotor"};
        String biggest = "";
        for (String s : arr) {
            if (isPalindrome(s) && s.length() > biggest.length()) {
                biggest = s;
            }
        }
        System.out.println("Biggest palindrome: " + biggest);
    }
}
```

---

### 12) Print numbers 1–10 without loops
Using recursion:
```java
public class PrintNumbers {
    public static void print(int n) {
        if (n > 10) return;
        System.out.println(n);
        print(n + 1);
    }
    public static void main(String[] args) {
        print(1);
    }
}
```

---

### 13) Movement commands
This seems incomplete. Could you clarify? If it’s about OS-level commands (like `cd`, `ls`, `mv`), or algorithmic movement (like robot/grid navigation), I can expand.

---

### 14) Run Spring Boot with non-embedded server
Yes. By default, Spring Boot uses embedded Tomcat/Jetty/Undertow. To run on an external server:
- Package as a **WAR** instead of JAR.
- Deploy WAR to external application server (Tomcat, WebLogic, JBoss).
- Configure `spring-boot-starter-tomcat` as `provided`.

---

### 15) What is method hiding?
- Occurs when a **static method** in a subclass has the same signature as one in the superclass.
- It’s not overriding, because static methods belong to the class, not the instance.
- The method invoked depends on the **reference type**, not the object type.

---

✅ These answers balance **technical correctness** with **interview-style clarity**.  
Would you like me to also **refine them into recruiter-friendly storytelling answers** (e.g., how you’d phrase #9 about Jira tickets to highlight your escalation-handling skills)? That way, you’ll sound both technically sharp and professionally mature.