pipeline {
  agent any
  
  stages {
    stage('Build and Test Frontend') {
      steps {
        dir('frontend') {
          sh 'npm install'
          sh 'npm run test'
          sh 'npm run build'
        }
      }
    }
    
    stage('Build Backend') {
      steps {
        dir('backend') {
          sh './mvnw clean package'
        }
      }
    }
  }
    