node {
     stage('Clone repository') {
         checkout scm
     }

     stage('Build image') {
          bat  'docker build -t k966/admin:contosoair$BUILD_NUMBER'
       
          
         echo '$BUILD_NUMBER'
     }
}
