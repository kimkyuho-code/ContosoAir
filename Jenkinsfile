node {
     stage('Clone repository') {
         checkout scm
     }

     stage('Build image') {
          bat  "docker build -t k966/admin:contosoair$BUILD_NUMBER ."
      }
     stage('Push image') {
          bat  "docker login -u 'k966' -p 'whdaud1224' docker.io"
          bat  "docker push k966/admin:contosoair$BUILD_NUMBER"
      }
}
