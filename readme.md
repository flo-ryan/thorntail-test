Minimal reproducer for an issue, when using the classes-jar of one Thorntail project as dependency in another, see  https://stackoverflow.com/questions/61369313/excluding-thorntail-dependencies-does-not-work-leading-to-weld-001408
* Java 8
* Thorntail 2.6.0
* Maven 3.6.1 (or 3.6.3)

### Project test1
* ```mvn clean install```

### Project test2
* ```mvn clean package```
* ```java -jar target/test2-thorntail.jar```

Remove or comment out the project1 classes-dependency in test2/pom.xml to get rid of the issue. 