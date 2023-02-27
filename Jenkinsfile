pipeline {
  agent any 
  tools {
    maven 'Maven'
  }
  stages {
    stage ('Initialize') {
      steps {
        sh '''
                    echo "PATH = ${PATH}"
            ''' 
      }
    }
     stage ('trufflehog scanning') {
      steps {
          sh 'pwd'
          sh 'echo $PATH'
          sh 'trufflehog3 https://github.com/satishcloudsec/WebGoat.git'
      }
     }
    
     stage ('Build') {
      steps {
          sh 'pwd'
          sh 'mvn clean package'
      }
     }
  }
}
