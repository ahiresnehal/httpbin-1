pipeline {
                          agent any
                            environment {  
                            registry = "docker.io/snehalahire123" 
                            registryCredential = 'dockerhub' 
                             dockerImage = ''
                                                 }
            stages {
                         stage('Hello') {
                                     steps {
                                               echo 'Hello World'
                                               }
                                               }
                         stage('git clone') {
                                              steps {
                                         git credentialsId: 'github', url: 'https://github.com/ahiresnehal/httpbin-1.git'
                                                        }
                                                        }
            
        stage('Docker Build and Tag') {
                                              steps {
                                                   //sh 'docker build -t nginxt:1.2 .' 
                                                     //sh 'docker build -t demo2:latest .' 
                                                     //sh 'docker tag demo2 snehalahire123/demo2:1.2'
                                                     //sh 'docker tag nginxte snehalahire123/nginxte:$BUILD_NUMBER'
                                                
                                                sh 'docker build -t nginxtest:1.2 .'
                                                 sh 'docker tag nginxtest snehalahire123/nginxtest:1.2'
                                                 sh 'docker tag nginxtest snehalahire123/nginxtest:$BUILD_NUMBER'
                                                       }
                                                       }
        stage('Publish image to Docker Hub') {
                                                          steps {
                                                             withDockerRegistry([ credentialsId: "dockerhub", url: "" ]) {
                                                             sh 'docker push snehalahire123/nginxtest:1.2'
                                                              //sh 'docker push snehalahire123/nginxte:$BUILD_NUMBER' 
                                                              }
                                                              }
                                                              }
        stage('deploy to rancher') {
                                       steps {
                                        script{
                                                 sh 'docker images'
                                                 sh 'ls'
                                                
                                                 }
                                                 }
                                                 }
  }
  }
