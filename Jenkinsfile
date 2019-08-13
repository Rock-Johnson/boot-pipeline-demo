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
        stash(includes: '**/target/*.jar', name: 'app')
      }
    }
    stage('docker build') {
      steps {
        unstash 'app'
        echo 'docker build'
        sh 'docker login -u rockzhaiy -p zhy13935889232 registry.cn-beijing.aliyuncs.com '
        sh 'pwd && ls'
        sh 'docker build -t registry.cn-beijing.aliyuncs.com/zhaiy/boot-pipeline-demo:1.0 .'
        sh 'docker push registry.cn-beijing.aliyuncs.com/zhaiy/boot-pipeline-demo:1.0'
        echo 'build end'
      }
    }
  }
}
