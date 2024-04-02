*Name*
__Cameron__
# Hi
## Hi 2
[Link]([http://a.com](https://ucsd-cse15l-s24.github.io/week1/index.html#lab-report-1---remote-access-and-filesystem-week-1))

![Image](dc1a7b120b1496b6badc84c874d61292.jpg)

> Hello world
* 1
* 2
* 3
1. One
2. Two
3. Three

Hello.java:

---
`Main` class
```
public class Hello {
  public static void main(String[] args) throws IOException {
    String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
    System.out.println(content);
  }
}
```
