HANDS ON 5 - Demonstration of Singleton Scope and Prototype Scope
====================================================================

Two XML configuration variants are provided:

1. country-singleton.xml
   - Default scope (singleton). Only ONE instance of the Country bean is
     created and shared for every context.getBean() call. The Country
     constructor is invoked only once.

2. country-prototype.xml
   - Same bean definition but with scope="prototype" added. A NEW instance is
     created every time context.getBean() is called. The Country constructor
     is invoked once per getBean() call (twice in this demo, since
     displayCountry() calls getBean() twice).

To switch between the two behaviors, use whichever XML file is loaded by
ClassPathXmlApplicationContext in displayCountry() (rename/copy the desired
file to "country.xml" on the classpath, or change the filename referenced in
the code).

Run the application with each configuration and observe the console logs:
  - Singleton scope: "Inside Country Constructor." appears once.
  - Prototype scope: "Inside Country Constructor." appears twice.
