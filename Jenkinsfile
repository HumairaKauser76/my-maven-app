pipeline {
  agent any
  tools {
    jdk 'JDK-17'
    maven 'Maven-3.9.11'
  }
  stages {
    stage('Checkout') {
      steps { checkout scm }
    }
    stage('Build') {
      steps { bat 'mvn clean package' }
    }
    stage('Run App') {
      steps {
        bat 'java -cp target/classes com.example.app.App'
      }
    }
  }
}
