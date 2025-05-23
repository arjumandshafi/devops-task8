TASK 8 - Java Maven Build with Jenkins

Objective:

Use Jenkins to build a simple Java application using Maven.

Tools Required:

- Jenkins (installed locally or via Docker)
  
- Docker desktop
  
- Java JDK 8 or 11
  
- Maven
  
- Git 

Steps:

Create a root directory:

mkdir hello-java-maven

then inside this directory create another directory:

mkdir src/main/java/HelloWorld.java

under src/main/java Create a Java HelloWorld App:

nano HelloWorld.java

2. Create a Maven Project File in root directory:
   
 cd hello-java-maven

in this directory write pom.xml file

nano pom.xml

3. Start Jenkins:

Using Docker desktop:

docker run -p 8080:8080 jenkins/jenkins:lts

4. Configure Jenkins:

- Go to "Manage Jenkins" → "Global Tool Configuration"
  
- Add Maven (e.g., Maven 3.8.6)

5. Create Jenkins Job:

- Create a new Freestyle Project
  
- In the "Build" section, choose "Invoke top-level Maven targets"
  
- Set Goals: clean package
  
- Save and build the job

6. Verify Build:

- Go to "Console Output"
  
- You should see: BUILD SUCCESS

Deliverables:

- Java HelloWorld app
  
- pom.xml file
  
- Jenkins job configuration
  
- Screenshot of successful build output
