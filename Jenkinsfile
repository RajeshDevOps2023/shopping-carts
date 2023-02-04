pipeline {
  agent any
  stages {
    stage('build-the-app1') {
      steps {
        echo 'this is the build job'
        sh 'mvn compile'
      }
    }

    stage('test-the-app1') {
      steps {
        echo 'this is the test job'
        sh 'mvn test'
      }
    }

    stage('package-the-app1') {
      steps {
        echo 'this is the package job'
        sh 'mvn package'
      }
    }

    stage('Archive Step') {
      steps {
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'maven'
  }
  post {
    always {
      echo 'this maven pipeline has completed...'
    }

  }
}