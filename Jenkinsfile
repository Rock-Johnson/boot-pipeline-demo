pipeline {
  agent any
  stages {
    stage('maven build') {
      agent {
        docker {
          image 'maven:3-alpine'
          args '''-v /root/.m2:/root/.m2
-v /data/maven:/usr/share/maven/ref/'''
        }

      }
      steps {
        sh 'mvn -s "/usr/share/maven/ref/settings-aliyun.xml" -B -DskipTests clean package'
      }
    }
    stage('docker build') {
      steps {
        node(label: 'build') {
          sh 'sidecar'
        }

      }
    }
  }
}