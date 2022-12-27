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
                                         git credentialsId: 'github', url: ''
                                                        }
                                                        }
            
        /*stage('Docker Build and Tag') {
                                              steps {
                                                   //sh 'docker build -t nginxt:latest .' 
                                                     sh 'docker build -t demo2:latest .' 
                                                     sh 'docker tag demo2 anjum1234/demo2:1.2'
                                                     //sh 'docker tag nginxte anjum1234/nginxte:$BUILD_NUMBER'
                                                       }
                                                       }
        stage('Publish image to Docker Hub') {
                                                          steps {
                                                             withDockerRegistry([ credentialsId: "dockerhub", url: "" ]) {
                                                             sh 'docker push anjum1234/demo2:1.2'
                                                              //sh 'docker push anjum1234/nginxte:$BUILD_NUMBER' 
                                                              }
                                                              }
                                                              }
        stage('deploy to rancher') {
                                       steps {
                                        script{
                                                 kubernetesDeploy (configs: 'deploymentservice.yaml', kubeconfigId: 'rancherconfih')
                                                 }
                                                 }
                                                 }*/
  }
  }
Footer
© 2022 GitHub, Inc.
Footer navigation
Terms

