HANDS ON 1 - Create a Spring Web Project using Maven
======================================================

These steps involve manual actions on https://start.spring.io/ and in Eclipse,
so they cannot be fully automated. Follow the steps below; the generated
project (as it should look after following these steps) is provided in the
"spring-learn" folder alongside this README for reference.

1. Go to https://start.spring.io/
2. Change Group to "com.cognizant"
3. Change Artifact Id to "spring-learn"
4. Select dependencies: Spring Boot DevTools, Spring Web
5. Click Generate to create and download the project as a zip
6. Extract the zip into your Eclipse Workspace root folder
7. Build the project from the command line:
     mvn clean package -Dhttp.proxyHost=proxy.cognizant.com -Dhttp.proxyPort=6050 ^
       -Dhttps.proxyHost=proxy.cognizant.com -Dhttps.proxyPort=6050 -Dhttp.proxyUser=123456
8. Import the project into Eclipse:
     File > Import > Maven > Existing Maven Projects > Browse to the extracted
     folder > Finish
9. Add a log statement to verify the main() method of SpringLearnApplication runs.
10. Run the SpringLearnApplication class.

Project walkthrough (SME to cover):
  - src/main/java   -> application source code
  - src/main/resources -> application configuration
  - src/test/java   -> test source code
  - SpringLearnApplication.java -> walk through the main() method
  - Purpose of the @SpringBootApplication annotation
  - pom.xml -> walk through all configuration; open 'Dependency Hierarchy' in
    Eclipse to view the dependency tree.

Folder contents:
  spring-learn/
    pom.xml
    src/main/java/com/cognizant/springlearn/SpringLearnApplication.java
    src/main/resources/application.properties
    src/test/java/com/cognizant/springlearn/SpringLearnApplicationTests.java
