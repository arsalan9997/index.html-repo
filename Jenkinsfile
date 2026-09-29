pipeline {
agent any

stages {

    stage('Checkout') {
        steps {
            git branch: 'master',
                url: 'https://github.com/dhruvikpatel892-design/index.html-repo.git'
        }
    }

    stage('Check HTML') {
        steps {
            sh 'ls -la'
            sh 'test -f index.html'
            echo 'index.html found successfully!'
        }
    }

    stage('Build') {
        steps {
            echo 'HTML project build completed successfully!'
        }
    }
}

post {
    success {
        echo 'Jenkins Pipeline SUCCESS!'
    }

    failure {
        echo 'Jenkins Pipeline FAILED!'
    }
}

}
