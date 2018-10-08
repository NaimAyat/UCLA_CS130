# Lecture 1: Oct 8, 2018
## 131 Review
* Polymorphism
* Subtyping
* Inheritance
```
interface I {
  void do();
}
class A implements I {
  void do() {
    // specific behavior for A;
  }
}
class B implements I {
  void do() {
    // specific implement pertinent to B;
  }
}
class Client {
  public void clientMethod() {
    I i = new A();
    // static type of i is I
    // runtime type is A
    A a = new A();
    // runtime type of a is A
  }
}

```
