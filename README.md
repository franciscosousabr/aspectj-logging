# aspectj-logging

This library allows logs to be generated automatically for method inputs and outputs, in addition to exception logs.

## Requirements

- Java 1.7+
- Spring Framework

## How to Use

For start, declare a Srping Bean like this:

```
@Bean
public LoggingAspect getLogging() {
  return new LoggingAspect();
}
```

So, in your method, add the `@EnableLogging` annotation.

```
@EnableLogging  
public String sayHello() {
  return "Hello";
}
```

The console shoud show this:

```
2020-07-02 15:31:23.611 DEBUG 25908 --- [tp291203641-258] br.com.leverinfo.logging.Test   : Entering on method "sayHello()"
2020-07-02 15:31:23.611 DEBUG 25908 --- [tp291203641-258] br.com.leverinfo.logging.Test   : Leaving method "sayHello()" with result: Hello
```