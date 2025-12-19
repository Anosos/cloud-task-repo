pipeline {
    agent any
    environment {
        FIREBASE_TOKEN = credentials('firebase-token')
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Deploy to Firebase') {
            steps {
                // ?????? ?????? ??????
                dir('GEM-Project') {
                    // ??????? bat ???? ?? sh ???? ??????
                    bat 'npx firebase-tools deploy --only hosting --token %FIREBASE_TOKEN% --project cloud-task-a8cb9'
                }
            }
        }
    }
}
