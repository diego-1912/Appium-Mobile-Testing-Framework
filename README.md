# Appium Page Object Model Framework

Appium mobile test automation framework with Page Object Model (POM) design using Java, Maven, and TestNG. This framework follows industry best practices and supports both Android and iOS within a single codebase.

## 📌 Objectives
This framework is designed to:

- Automate mobile applications using Appium
- Implement the Page Object Model (POM) for maintainability and scalability
- Support parallel execution on multiple real devices
- Integrate logging, reporting, and test management tools
- Handle test data abstraction with JSON & XML
- Provide explicit waits and exception handling mechanisms
- Improve test reusability and readability

## 📁 Folder Structure
The following is the directory structure of the project and their purposes:

```
APPUIUM-PAGEOBJECTMODEL-MASTER/
│── src/
│   ├── main/
│   │   ├── resources/                 # Configuration files
│   │   │   ├── config.properties       # Global configuration properties
│   │   │   ├── log4j2.xml              # Logging configuration
│   │── test/
│   │   ├── java/com/qa/                # Main test automation package
│   │   │   ├── listeners/              # Custom TestNG listeners for test execution tracking
│   │   │   │   ├── TestListener.java   # Implements TestNG listener methods
│   │   │   ├── pages/                  # Page Object Model (POM) classes
│   │   │   │   ├── LoginPage.java
│   │   │   │   ├── ProductDetailsPage.java
│   │   │   │   ├── ProductsPage.java
│   │   │   │   ├── SettingsPage.java
│   │   │   ├── reports/                # Reporting utilities
│   │   │   │   ├── ExtentReport.java   # Generates Extent Reports
│   │   │   ├── tests/                  # Test cases
│   │   │   │   ├── LoginTests.java
│   │   │   │   ├── ProductTests.java
│   │   │   ├── utils/                   # Utility functions
│   │   │   │   ├── TestUtils.java       # Common helper functions
│   │   │   │   ├── BaseTest.java        # Base test setup and teardown
│   │   │   ├── MenuPage.java            # Common menu navigation actions
│── resources/                           # External test data and applications
│   ├── app/                             # Mobile applications under test
│   ├── data/                            # Test data storage
│   ├── strings/                         # Static text localization
│── target/                              # Compiled test results and reports
│── .gitignore                           # Git ignore file
│── pom.xml                              # Maven project configuration
│── testing.xml                          # TestNG execution configuration
│── README.md                            # Project documentation
```

## 📚 Technologies & Tools Used

- **Programming Language:** Java
- **Test Framework:** TestNG
- **Automation Library:** Appium
- **Build Tool:** Maven
- **Logging:** Log4J2
- **Reporting:** Extent Reports
- **Version Control:** GitHub
- **Continuous Integration:** Jenkins
- **Test Data:** JSON / XML

## 🔧 Prerequisites
Ensure you have the following installed before setting up the project:

- Java 8+ - [Download & Install Java](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html)
- Maven - [Download & Install Maven](https://maven.apache.org/download.cgi)
- Appium Server - [Download & Install Appium](https://appium.io/)
- Node.js (Required for Appium) - [Download Node.js](https://nodejs.org/)
- Android SDK (for Android testing) - Install via Android Studio
- Xcode (for iOS testing) - Download from Mac App Store (MacOS only)
- Git - [Download & Install Git](https://git-scm.com/)

## 🛠 Installation & Setup
Follow these steps to set up the framework:

### 1️⃣ Clone the Repository
```sh
git clone https://github.com/your-repo/appium-pageobjectmodel.git
cd appium-pageobjectmodel
```

### 2️⃣ Install Dependencies
```sh
mvn clean install
```

### 3️⃣ Start Appium Server
```sh
appium
```
Ensure your mobile device or emulator is running before executing tests.

### 4️⃣ Configure Devices
Modify `config.properties` file under `src/main/resources` to specify:
```properties
platformName=Android/iOS
deviceName=emulator/device
appPath=path_to_apk_or_app_file
```

## ▶️ Running Test Cases
You can run tests using TestNG or Maven.

### 1️⃣ Run Tests via TestNG
```sh
mvn test
```
Or
```sh
mvn test -DsuiteXmlFile=testing.xml
```

### 2️⃣ Run a Specific Test Class
```sh
mvn -Dtest=LoginTests test
```

### 3️⃣ Run Parallel Execution
Modify `testing.xml` to enable parallel execution and run:
```sh
mvn test -Dsurefire.suiteXmlFiles=testing.xml
```

## 📊 Test Reports
The framework generates Extent Reports automatically after execution. You can find the report in:
```sh
target/ExtentReports/index.html
```
Open this file in a browser to view detailed test execution logs, screenshots, and results.


🚀 **Happy Testing with Appium & Java!** 🚀
