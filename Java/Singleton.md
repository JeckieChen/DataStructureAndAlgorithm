# 饿汉式
```java
public class Singleton{
  private final static Singleton INSTANCE = new Singleton();
  private Singleton(){}
  public static Singleton getInstance(){
    return INSTANCE;
  }
}
```

# 懒汉式
```java
public class Singleton {

    private static Singleton instance = null;

    private Singleton() {
    }

    public static synchronized Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }

}

```
