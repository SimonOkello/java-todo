pipeline { 
  agent any
  tools { 
    gradle "Gradle-8"
  }
  stages { 
    stage('clone repository') {
      steps { 
        echo 'Cloning todo app'
        git 'https://github.com/SimonOkello/java-todo.git'
      }
    }
    stage('Build the project') {
      steps { 
        echo 'Building the app'
        sh 'gradle build'
      }
    }
    stage('Tests') {
      steps { 
        echo 'Testing the app'
        sh 'gradle test'
      }
    }
  }
}