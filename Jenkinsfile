pipeline {
    agent any

    tools {
        maven 'Maven 3.6.3'  // Configure this according to your Jenkins Maven installation
        jdk 'JDK 11'         // Configure this according to your Jenkins JDK installation
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                // Déployez votre application si nécessaire, par exemple en copiant le jar ou en exécutant un script de déploiement
                echo 'Deploy stage - Add deployment steps here'
            }
        }
    }
}
