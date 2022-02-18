pipeline {
    agent any
 stages {
  stage('Docker Build and Tag') {
           steps {
              
                sh 'docker build -t nginxtest:latest .' 
<<<<<<< HEAD
                sh 'docker tag nginxtest nikhilnidhi/nginxtest:latest'
                sh 'docker tag nginxtest nikhilnidhi/nginxtest:$BUILD_NUMBER'
=======
                sh 'docker tag nginxtest nbrico/nginxtest:latest'
                sh 'docker tag nginxtest nbrico/nginxtest:$BUILD_NUMBER'
>>>>>>> 1a539b56fbf5fc3b4973aa721dd7a01dbf9884f3
               
          }
        }
     
  stage('Publish image to Docker Hub') {
          
            steps {
        withDockerRegistry([ credentialsId: "dockerHub", url: "" ]) {
<<<<<<< HEAD
          sh  'docker push nikhilnidhi/nginxtest:latest'
          sh  'docker push nikhilnidhi/nginxtest:$BUILD_NUMBER' 
=======
          sh  'docker push nbrico/nginxtest:latest'
          sh  'docker push nbrico/nginxtest:$BUILD_NUMBER' 
>>>>>>> 1a539b56fbf5fc3b4973aa721dd7a01dbf9884f3
        }
                  
          }
        }
     
      stage('Run Docker container on Jenkins Agent') {
             
            steps {
<<<<<<< HEAD
                sh "docker run -d -p 4030:80 nikhilnidhi/nginxtest"
=======
                sh "docker run -d -p 4030:80 nbrico/nginxtest"
>>>>>>> 1a539b56fbf5fc3b4973aa721dd7a01dbf9884f3
 
            }
        }
 stage('Run Docker container on remote hosts') {
             
            steps {
<<<<<<< HEAD
                sh "docker -H ssh://jenkins@172.31.28.25 run -d -p 4001:80 nikhilnidhi/nginxtest"
=======
                sh "docker -H ssh://jenkins@192.168.1.201 run -d -p 4001:80 nbrico/nginxtest"
>>>>>>> 1a539b56fbf5fc3b4973aa721dd7a01dbf9884f3
 
            }
        }
    }
}
