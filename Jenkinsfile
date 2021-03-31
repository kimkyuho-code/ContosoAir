node {
     stage('Clone repository') {
         checkout scm
     }

     stage('Build image') {
          bat  "docker build -t k966/admin:contosoair$BUILD_NUMBER ."
      }
     
     stage('Push image') {
          
           docker.withRegistry('https://registry.hub.docker.com', 'docker-hub') {
             app.push("${env.BUILD_NUMBER}")
             app.push("latest")
           }
 
      }
}
