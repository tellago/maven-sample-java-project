def output = 'maven'
def x = '10'
pipeline {
    agent any
        
        stages {
        stage('checkout') {
            steps {
              git 'https://github.com/tellgo/maven-sample-java-project.git'
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
