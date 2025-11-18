#### This project is for the Devops bootcamp exercise for 
#### "Build Tools and Package Managers" 

# Exercises for Module "Build Tools and Package Manager" 

Use repository: https://gitlab.com/twn-devops-bootcamp/latest/04-build-tools/build-tools-exercises

🔸 [EXERCISE 0: Clone project and create own Git repository]

To work with the project for the exercises:

✅ How to Clone the Provided Project and Create Your Own Git Repository

You were given this repository:
https://gitlab.com/twn-devops-bootcamp/latest/04-build-tools/build-tools-exercises

Your task:

### - Clone that project
    git clone https://gitlab.com/twn-devops-bootcamp/latest/04-build-tools/build-tools-exercises
### - Move into the folder:
    cd build-tools-exercises
### - Remove the Original Git History
    rm -rf .git
### - Create your own project/repository using its content
   git init
   git add .
   git commit -m "Initial commit based on build-tools-exercises"
### — Create Your Own Remote Repository

Depending on where you want your new repo:
If using GitLab
Go to GitLab ➜ “New Project”
Create an empty repository
Copy the remote URL, e.g.:

https://gitlab.com/your-username/your-new-repo.git


### - Add it as your remote:

    git remote add origin https://gitlab.com/your-username/your-new-repo.git

### - Push your project:

    git push -u origin main

🔸 [EXERCISE 1: Build jar artifact]

You want to deploy the artifact to share that library with all team members. So:

### - try to build the jar file
    gradle build

The Build will fail, because of a compile error in a test, so you can't build the jar.

🔸 [EXERCISE 2: Run tests]

#### - Fix the test, by changing "true" string to true boolean.
     boolean result = myApp.getCondition(true);

#### - Run gradle test to execute only the tests and check the fix.
     gradle test

🔸 [EXERCISE 3: Clean and build App]

You fixed the test. Now:

#### - clean the build folder with gradle clean and

This will delete the entire build/ directory:

    gradle clean

#### - Build the JAR file again: 

    gradle build
This will:
  1. compile your Java source
  2. run your tests
  3. package your app
  4. produce the JAR file

JAR will appear here:

    build/libs/

🔸 [EXERCISE 4: Start application]

Start the jar file to test that the application runs successfully as a jar file

#### - Start app with /build/libs java -jar app-1.0.jar
NOTE: replace "app-1.0.jar" with the name of YOUR jar file.

     java -jar build/libs/build-tools-exercises-1.0-SNAPSHOT.jar 

🔸 [EXERCISE 5: Start App with 2 Parameters]
Now you want to add parameters to your application, so you and other users can pass different values on startup.

Add parameter input to the Java code (see code snippet below, which you can copy)
Rebuild the jar file
Execute the jar file again with 2 params

 Code snippet for Exercise 5!
 Code snippet to add inside Application.java on line 16

    Logger log = LoggerFactory.getLogger(Application.class);

     try {
           String one = args[0];
           String two = args[1];
           log.info("Application will start with the parameters {} and {}", one, two);
     } catch (Exception e) {
          log.info("No parameters provided");
     }

    gradle clean 
    gradle build
    java -jar build/libs/build-tools-exercises-1.0-SNAPSHOT.jar hello world

### 2025-11-18T11:33:24.587+02:00  INFO 15245 --- [           main] com.example.Application                  : Application will start with the parameters hello and world
                                                                                                                 
   
