def output = 'maven'
def x = '10'
pipeline {
    agent any
    
            stages {
        stage('Checkout Codebase'){
            steps{
                checkout scm: [$class: 'GitSCM', branches: [[name: '*/master']], userRemoteConfigs: [[credentialsId: 'PUBLIC_KEY', url:' https://github.com/tellago/maven-sample-java-project.git']]]
                               }
                               }
        stage('Hello') {
            steps {
                echo "Hello World ${output}"
            }
        }
        stage('sample-test') {
            steps {
                echo "Print value ${x}"
            }
        }
                pipeline {
                    
                agent any

    stages {

        stage('Build') {

            steps {
                sh 'github.com/tellago/maven-sample-java-project.git'
            }
        }
    }
                }
               stage('validate') {
               steps {
               sh 'mvn validate'
            }
          }
        stage('compile') {
          steps {
            sh 'mvn compile'
          }
        }
        stage('test') {
          steps {
            sh 'mvn test'
          }
        }
        stage('package') {
          steps {
            sh 'mvn package'
          }
        }
    }
}

