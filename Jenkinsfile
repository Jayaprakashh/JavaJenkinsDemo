pipeline {
	
    agent any

    environment {
        JAVA_HOME = "C:\\Program Files\\Java\\jdk-17"  // Update if needed
        PATH = "${JAVA_HOME}\\bin;${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Jayaprakashh/JavaJenkinsDemo.git'  // Update with your GitHub repo
            }
        }

        stage('Compile Java') {
            steps {
                bat 'javac -d out src/com/javajenkins/DemoJenkins.java'  // Compile Java file
            }
        }

        stage('Run Java Program') {
            steps {
                bat 'java -cp out com.javajenkins.DemoJenkins'  // Run Java program
            }
        }
    }
}
