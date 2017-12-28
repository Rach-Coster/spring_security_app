# spring_security_app
A security app I made with this tutorial: https://spring.io/guides/gs/securing-web/

#How to use:
- get the terminal to locate the folder you have cloned
- run gradlew bootRun in the terminal 
- go to localhost:8080 to see the applet
- to login use the username: username and the password: password

#Issues I had: 
- The error detection while running bootRun with gradlew was abysmal at best. Errors would be too ambiguous and there was minimal documentation on what to do when an error occured. This left my standed for hours scouring the internet, trying to find an answer. 
- The file directory had to be exact or else gradlew bootRun would not work however, I could use the build and clean functions just fine. 
- For the java files the directory is: 
  - Name of project
    - src 
      - main
        - java 
          - hello (or any other package name of your choosing. I just stuck with the default name for my own sanity) 
- For the html files the directory is: 
  - Name of project
    - src
      - main
        - resources 
          - templates
- Build.gradle is still a pain in the neck especially on build. I needed to add the following lines of code to get it working: 
  - apply plugin: 'application'
  - compile("org.springframework.boot:spring-boot-starter-thymeleaf") <- (This is for the dependencies{ } area) 
  - springBoot {
      mainClass = "Application.java"
    } <- (I didn't end up needed this function but I thought I'd include it just in case some other poor person on the internet was having a similar issue)
    
