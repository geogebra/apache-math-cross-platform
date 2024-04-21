pipeline {
    agent {
        label 'Ubuntu'
    }
    environment {
        MAVEN = credentials('maven-repo')
        LANG = 'en_US.UTF-8'
        LC_ALL = 'en_US.UTF-8'
    }
    stages {
        stage('Build'){
            steps {
                sh 'sh ./gradlew publish'
            }
        }
    }

    post {
        always { cleanAndNotify() }
    }
}

