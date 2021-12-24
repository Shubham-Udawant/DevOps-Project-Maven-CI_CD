DevOps-Project: Maven CI/CD, schedule task and Source code polling
-----------------------------------------------------------------
Description / Steps:

Tools: EC2, Maven, Git, Github, Java 

1. Install the Git and configure on the machine.
2. Install the Java and configure the environment varible on the machine.
3. Install the Maven and configure the environment varible on the machine.
4. Install the Jenkins and install the required plugins inside it.
   manage jenkins --> manage plugins --> maven integration & green balls --> install without restart,
   manage jenkins --> global tool configuration --> add JDK --> uncheck the install automatically option, 
5. Clone the Github repo to local machine.
   go inside the clone repo --> run the (#mvn clean package) it convert the code into machine level language,
6. Maven project (by Jenkins)   
   Jenkins --> new item --> enter name (myMavenProject) --> select Maven project --> ok,
   source code management --> git --> < copy github repo URL & paste >,
   build --> root POM --> pom.xml,
   goals & option --> clean package --> save,
   jenkins --> myMavenProject --> build now,
7. Schedule Project
   myMavenProject --> configure --> build triggers --> build periodically --> ***** --> save,
8. Source code polling
   myMavenProject --> configure --> build triggers --> click on poll SCM --> schedule --> ***** --> save (now it build automatically)
