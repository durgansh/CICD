pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                                   '''
      }
    }
    stage('Build') {
      steps {
        dir("/opt/CICD/HelloWorld/recipes") {
          sh 'mvn -Dmaven.test.failure.ignore=true -U clean install'
        }

      }
    }
    
  }
}
