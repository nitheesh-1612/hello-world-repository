pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
        stage ('Build') {
            steps {
                sh 'mvn clean package'
            }
        post {
            success {
                echo "build is success"
            }
            failure {
                echo "build is faileddddd"
            }
        }  
        }
      stage ('run') {
          steps {
              sh 'java -cp target/helloworld-1.0.jar com.coveros.demo.helloworld.HelloWorld'
      }
      
    }
}
