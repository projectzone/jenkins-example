pipeline {
    agent Centos_201

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3.3.3') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3.3.3') {
                    sh 'mvn test'
                }
            }
        }


        stage ('install Stage') {
            steps {
                withMaven(maven : 'maven_3.3.3') {
                    sh 'mvn install'
                }
            }
        }
    }
}
