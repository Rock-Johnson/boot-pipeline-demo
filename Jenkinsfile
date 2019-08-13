pipeline {
  agent any
  stages {
    stage('maven build') {
      agent {
        docker {
          image 'maven:3-alpine'
          args  '-v /root/.m2:/root/.m2'
        }

      }
      steps {
        sh 'mvn -s "/usr/share/maven/ref/settings-aliyun.xml" -B -DskipTests clean package'
      }
    }
  }
}