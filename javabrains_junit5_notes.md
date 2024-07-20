
The point of writing automated tests **_not so much_ that to _verify that code works now_, but** it is **_to verify on ongoing basis_ that _code continues to work in future_.**  

#### Why use Testing Framework?

To run programmatic unit tests, we need following things:
- Preparation
- Provide test inputs
- Run tests
- Provide expected output
- Verify result
- Do something to alert developer if test failed

Of all above things, below are going to be **different** for each execution
- Preparation
- Provide test inputs
- Provide expected output


and below things are going to **common** for each execution
- Run tests
- Verify result
- Do something to alert developer if test failed

> [!IMPORTANT]
> JUnit5 Framework provide all above things out of box


#### JUnit 5 Architecture


![image](https://github.com/user-attachments/assets/4d2ac9d3-3864-4067-9694-14efe0faff41)







#### JUnit 5 Dependencies

```
  <junit.jupiter.version>5.8.2</junit.jupiter.version>

  <dependencies>
    <dependency>
      <groupId>org.junit.jupiter</groupId>
      <artifactId>junit-jupiter-engine</artifactId>
      <version>${junit.jupiter.version}</version>
      <scope>test</scope>
    </dependency>
    <dependency>
      <groupId>org.junit.jupiter</groupId>
      <artifactId>junit-jupiter-api</artifactId>
      <version>${junit.jupiter.version}</version>
      <scope>test</scope>
    </dependency>
  </dependencies>

```

> [!NOTE]
> Dependencies with `<scope>test</scope>` are not included in final build.















