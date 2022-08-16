# PROJECT-14-ansible-configuration-management
PROJECT-14-ansible-configuration-management
====================================
 #### Jenkin file for quick task :
 ===================================
 ```
    pipeline {
    agent any

  stages {
    stage("Initial cleanup"){
      steps {
        dir("${WORKSPACE}"){
          deleteDir()
        }
      }
    }
    
     stage('Build') {
       steps {
         script {
          sh 'echo "Building Stage"'
        }
      }
    }

    stage('Test') {
      steps {
        script {
          sh 'echo "Testing Stage"'
        }
      }
    }
    stage('Package') {
      steps {
        script {
          sh 'echo "Packaging Stage"'
        }
      }
    }
    stage('Deploy') {
      steps {
        script {
          sh 'echo "Deploying Stage"'
        }
      }
    }
    stage('Clean up') {
      steps {
        cleanWs()
        }
      }
   
    }
  }
   
```