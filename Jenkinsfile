pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code berhasil diambil dari GitHub'
            }
        }

        stage('Build') {
            steps {
                sh 'ls -lah'
                sh 'test -f index.html'
                echo 'Build portfolio berhasil'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Simulasi deploy berhasil'
            }
        }
 
   }
}
