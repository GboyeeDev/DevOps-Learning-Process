# Build Tools Exercises Project

This repository contains the completed exercises for the Build Tools and Package Manager module. The project demonstrates building, testing, and running a Java helper library using Gradle, with detailed steps for each exercise.

---

## Table of Contents
1. [Exercise 0: Clone Project and Create Own Git Repository](#exercise-0-clone-project-and-create-own-git-repository)
2. [Exercise 1: Build JAR Artifact](#exercise-1-build-jar-artifact)
3. [Exercise 2: Run Tests](#exercise-2-run-tests)
4. [Exercise 3: Clean and Build App](#exercise-3-clean-and-build-app)
5. [Exercise 4: Start Application](#exercise-4-start-application)
6. [Exercise 5: Start App with Parameters](#exercise-5-start-app-with-parameters)
7. [Notes and Troubleshooting](#notes-and-troubleshooting)

---

## Exercise 0: Clone Project and Create Own Git Repository

### Steps:
1. Clone the project:
   ```bash
   git clone https://gitlab.com/twn-devops-bootcamp/latest/04-build-tools/build-tools-exercises
   cd build-tools-exercises
   ```

2. Initialize a new Git repository:
   ```bash
   git init
   git add .
   git commit -m "First commit for build tool project"
   ```

3. Create a new repository on GitHub or GitLab.
4. Add the new repository as the remote origin:
   ```bash
   git remote add origin https://github.com/<your-username>/build-tools-project.git
   ```

5. Push the code to your repository:
   ```bash
   git branch -M main
   git push -u origin main
   ```

---

## Exercise 1: Build JAR Artifact

### Steps:
1. Attempt to build the JAR file:
   ```bash
   ./gradlew build
   ```

2. **Expected Outcome:**
    - The build fails due to a compile error in a test file.

---

## Exercise 2: Run Tests

### Steps:
1. Locate the test causing the error (e.g., `src/test/java/...`).
2. Fix the issue by replacing the incorrect `"true"` string with the correct `true` boolean:
   ```java
   assertEquals(true, someCondition);
   ```

3. Run the tests to verify the fix:
   ```bash
   ./gradlew test
   ```

4. Ensure all tests pass.

---

## Exercise 3: Clean and Build App

### Steps:
1. Clean the build directory:
   ```bash
   ./gradlew clean
   ```

2. Rebuild the JAR file:
   ```bash
   ./gradlew build
   ```

3. Verify the generated JAR file in the `build/libs/` directory.

---

## Exercise 4: Start Application

### Steps:
1. Run the application JAR file:
   ```bash
   java -jar build/libs/app-1.0.jar
   ```

2. Verify the output to ensure the application starts successfully.

---

## Exercise 5: Start App with Parameters

### Steps:
1. Modify the Java code to accept parameters:
    - Open `src/main/java/.../Application.java`.
    - Add the following snippet inside the `main` method:
      ```java
      Logger log = LoggerFactory.getLogger(Application.class);
      try {
            String one = args[0];
            String two = args[1];
            log.info("Application will start with the parameters {} and {}", one, two);
      } catch (Exception e) {
            log.info("No parameters provided");
      }
      ```

2. Rebuild the JAR file:
   ```bash
   ./gradlew build
   ```

3. Run the application with parameters:
   ```bash
   java -jar build/libs/app-1.0.jar param1 param2
   ```

4. Verify the output displays the parameters:
   ```
   Application will start with the parameters param1 and param2
   ```

5. Test running the app without parameters:
   ```bash
   java -jar build/libs/app-1.0.jar
   ```
    - **Expected Output:**
      ```
      No parameters provided
      ```

---

## Notes and Troubleshooting

### Common Issues:
1. **`gradlew` Not Recognized:**
    - Use `gradlew.bat` for Windows:
      ```bash
      gradlew.bat build
      ```

2. **Java Version Incompatibility:**
    - Ensure Java 17 or newer is installed.
    - Set `JAVA_HOME` to the correct JDK path.

3. **Gradle Version Update:**
    - If required, update the Gradle wrapper version in `gradle-wrapper.properties`:
      ```properties
      distributionUrl=https\://services.gradle.org/distributions/gradle-8.10-bin.zip
      ```

4. **Dependency Issues:**
    - Verify all dependencies in `build.gradle` are compatible with your Java version.

---

## Completed Task Checklist
- [x] Clone project and create a new repository.
- [x] Fix test errors and run tests.
- [x] Build JAR file successfully.
- [x] Start the application.
- [x] Add parameter support and test the application with parameters.

---

## Project Details
- **Language:** Java
- **Build Tool:** Gradle
- **Java Version:** 17+
- **Completed By:** GboyeeDev
