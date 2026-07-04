pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                dir('Task_14/owasp-jenkins-demo') {
                    sh 'mvn clean verify'
                }
            }
        }

        stage('OWASP Scan') {
            steps {
                dir('Task_14/owasp-jenkins-demo') {
                    sh 'mvn org.owasp:dependency-check-maven:check'
                }
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'Task_14/owasp-jenkins-demo/target/dependency-check-report.html', fingerprint: true
        }
    }
}
