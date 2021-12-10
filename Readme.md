## ℹ️ About Project

This project is about creating mobile test automation scenarios building a framework with recent technologies.

<h3 align="center">We are 2nd place in that Hackhaton with this project <img width="20px" height="20px" src="https://cdn.icon-icons.com/icons2/2526/PNG/512/trophy_cup_second_award_icon_151772.png"></h3>
<br/>
Our team name is : **SahiMobi** and has 4 members to attend that [Hackhaton](https://mobven.atlassian.net/wiki/spaces/TH/overview), and developed together. 

Thanks to my friends; 
<br/>
- [Enes Aydın](https://github.com/enesaydinqa)
- [Burak Ergören](https://github.com/burakergoren)
- [Nahide Ergün](https://github.com/nahidErgun)

Total 3 scenarios developed via Appium libraries with Android platform. In addition, this project has 4 modules.
    
    Application Name: Airbnb android version
    Devices: Samsung Galaxy S21, Samsung Galaxy A51 (You can use emulator or your real devices)

- First Module: `Hackhaton Parent` --> Keeps project dependencies
- Second Module: `Hackhaton Core` --> Keeps Appium-JUnit-Reporting core framework codes
- Third Module: `airbnb-android-test` --> Keeps 3 Airbnb test scenarios
- Fourth Module: `jenkins, jenkins-file` --> Devops, Docker and Jenkins configurations are implemented

#####Scenario Informations:

1) AirBnbAddFavoriteTest: Search a city and then find a place add to Favorite List.
2) AirBnbLoginTest: Login a sample user
3) AirBnbRemoveFavoriteTest: Delete added favorite item from list. 

## Used Technologies

- Java 11
- Docker for supporting infrastructure
- Maven for dependencies
- Appium - Selenium
- JUnit 5 for test framework
- JIRA for tracking Bug/Defect Management
- Jenkins for CI/CD processes
- Github for version controlling
- ExtentReport for reporting structure
- SonarQube for improving code quality
- H2 with powered Hibernate for storing data

## 🚀 How to use

- Install packages with  `docker compose.yaml`
- Run `docker-compose up` for start to Jira, Jenkins, SonarQube for infrastructure. These tools are configured with same network to communicate with each other and their own persistent volumes in order to keep data's.
- Open the `http://localhost:8081/` to access Jenkins.. Default username and password is: admin
- Open the `http://localhost:8082/` for Jira. Do not forget to setup Jira after accessing the URL. Jira needs a commercial key for licensing but also can get a trial key.
- Finally, `http://localhost:9000/` is also for SonarQube. Default username and password is: admin. Generate a token for Jenkins Integration.

- If you want to run tests in Dockerized environment, open the Jenkins URL and Build relevant pipeline. That's it :)
- If you want to run tests in locally, open the project in IDE, select related class and Run it. Pretty simple :)

## 🗒️ Additional Informations

You can get detail informations in below:

    . This framework is powered with SpringBoot and JUnit 5 using Java 11. That's why you can create your custom extensions to manage framework as you need.

    . In addition, Jenkins works as a `Configuration As Code`. That means, in the project there is a `jenkins-casc.yml` file in jenkins folder for configuration of it.

    . Jenkins Pipeline configuration is located in jenkins-file folder in project.

    . Furthermore, When the test will fail, system get screenshot of related step and get stack trace informations send to JIRA for creating a issue to handle Bug/Defect management.

    . ExtentReport is implemented in project for reporting with screeshots and detailed logs.

    . Implemented shell scripts for managing Real/Emulator Android devices for connection to run tests in locally or Docker Containers. This configuration runs dynamically. If device count will change, system automatically understand how many devices connected for mobile testing.

    . H2 database for keeping test data's and also system informations to supply sustainability.

    . ScreenshotTaker contains failed scenarios screenshot process and stores screenshot folder in base project path.
