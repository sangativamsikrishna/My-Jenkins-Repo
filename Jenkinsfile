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
  }
}
