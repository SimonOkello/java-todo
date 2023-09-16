pipeline { 
  agent any
  tools { 
    gradle "Gradle-8"
  }
  stages { 
    stage('clone repository') {
      steps { 
        git 'https://github.com/SimonOkello/java-todo.git'
      }
    }
    stage('Build the project') {
      steps { 
        sh 'gradle build'
      }
    }
    stage('Tests') {
      steps { 
        sh 'gradle test'
      }
    }
  }
}