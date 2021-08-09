pipeline {
    agent any
    
    tools {
    jdk 'JAVA_8'
    maven 'Maven 3.3.3'
  }

    stages {
        stage ('Compile Stage') {

             steps {
                    echo 'Hello World'
            
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
