pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Memeriksa file website...'
                sh 'test -f index.html'
                sh 'test -f style.css'
                sh 'test -f script.js'
                sh 'ls -la'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy seluruh file dan folder website...'
                sh '''
                    rsync -av --delete \
                        --exclude='.git/' \
                        --exclude='Jenkinsfile' \
                        ./ /var/www/portfolio-jamal/
                '''
            }
        }
    }

    post {
        success {
            echo 'Deploy website berhasil!'
        }
        failure {
            echo 'Deploy website gagal!'
        }
    }
}
