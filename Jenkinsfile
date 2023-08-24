pipeline {
agent any
stages {
    stage ("Build httpd Image") {
    steps {
      sh 'sudo docker build -t httpd02 .'
      sh 'sudo docker ps'
    }
  }
  
  stage ("Delivery of Image to Docker Hub") {
    steps {
      sh 'sudo docker image tag httpd02 susigugh/httpd02:1.0'
      sh 'sudo docker push susigugh/httpd02:1.0'
    }
  }
  
}
}
