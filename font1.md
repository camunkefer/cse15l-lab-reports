*Name*
__Cameron__
# Hi
## Hi 2
[Link](http://a.com)
![Image](http://url/a.png)
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
