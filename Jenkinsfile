pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
        stage('Lint')
            steps {
                sh 'npm run lint'
                sh 'npm run lint:config -- -f ./config/7ms.yml'
                sh 'npm run lint:config -- -f ./config/addo.yml'
                sh 'npm run lint:config -- -f ./config/addo.yml'
                sh 'npm run lint:config -- -f ./config/ctf.yml'
                sh 'npm run lint:config -- -f ./config/default.yml'
                sh 'npm run lint:config -- -f ./config/fbctf.yml'
                sh 'npm run lint:config -- -f ./config/juicebox.yml'
                sh 'npm run lint:config -- -f ./config/mozilla.yml'
                sh 'npm run lint:config -- -f ./config/oss.yml'
                sh 'npm run lint:config -- -f ./config/quiet.yml'
                sh 'npm run lint:config -- -f ./config/tutorial.yml'
                sh 'npm run lint:config -- -f ./config/unsafe.yml'
            }
    }
}