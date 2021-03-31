node {
     stage('Clone repository') {
         checkout scm
     }

     stage('Build image') {
         app = docker.build("k966/admin:contosoair:$BUILD_NUMBER") 
     }
}
