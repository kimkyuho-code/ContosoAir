node {
     stage('Clone repository') {
         checkout scm
     }

     stage('Build image') {
         
          app = docker.build("k966/admin:contosoair")
      }
     
     stage('Push image') {
          
           docker.withRegistry('https://registry.hub.docker.com', 'docker-hub') {
      
            app.push("contosoair${env.BUILD_NUMBER}")
               
           }
 
      }
}
