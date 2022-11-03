//Jenkins file only to tutorial example
pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages{        
    stage('Cloning Git'){
      steps{
        git 'https://github.com/JVMatos/jenkins-node-test'
      }
    }
    stage('Install dependencies'){
      steps{
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('build'){
      steps{
        sh 'npm run build'
      }
    }
    stage('Deliver') { 
      steps {
        sh 'npm start'
      }
    }
  }
}
