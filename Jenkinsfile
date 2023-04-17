pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        // Clone the code repository
        git 'https://github.com/sangativamsikrishna/My-Jenkins-Repo.git'

        // Compile the code using Maven
        sh 'mvn clean package'
      }
    }
    
    stage('Test') {
      steps {
        // Run automated tests using Maven
        sh 'mvn test'
      }
    }
    stage('Deploy') {
      steps {
        // Deploy the application to a Tomcat server
        sh 'scp /var/lib/jenkins/workspace/reddy/target/helloworld-1.0-SNAPSHOT.jar ubuntu@ 52.23.165.243:/home/ubuntu/apache-tomcat-9.0.73/webapps/manager'
  }
}
