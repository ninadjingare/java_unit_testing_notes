
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
> JUnit 5  testing framework provide all above things out of box


#### JUnit 5 Architecture


![image](https://github.com/user-attachments/assets/4d2ac9d3-3864-4067-9694-14efe0faff41)







#### JUnit 5 Dependencies

- `junit-jupiter-api`   API for writing tests using JUnit Jupiter
- `junit-jupiter-engine` Implementation of the TestEngine API for JUnit Jupiter
- `junit-vintage-engine` A thin layer on top of JUnit 4 to allow running vintage tests


```xml
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



`@Test`
+ Marks method as a Test
+ Informs the JUnit engine what method needs to run


##### Expectation vs Reality

* Create an instance of class under test
* Set up inputs
* Execute the code you want to test
* Verify the result is what you expect


> [!NOTE]
> assert:  to say something clearly and firmly

#### Test Life Cycle
Test Life Cycle is a process in which test instance is created, managed and destroyed.

![image](https://github.com/user-attachments/assets/87b729bb-09fa-49c1-983a-c914126d1347)




##### Life Cycle Hooks
+ `@BeforeAll`
+ `@AfterAll`
+ `@BeforeEach`
+ `@AfterEach`

#### Annotations to scale your tests

- `@DisplayName`
- `@Disabled`

#### Conditional Executions

- `@EnabledOnOs(OS.LINUX)`
- `@EnabledOnJre(JRE.JAVA_11)`
- `@EnabledIf`
- `@EnabledIfSystemProperty`
- `@EnabledIfEnvironmentVariable`















