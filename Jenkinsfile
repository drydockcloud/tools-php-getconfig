pipeline {
    agent any
    stages {
        stage('Code linting') {
            steps {
                script {
                    // Lint PHP using php-cs-fixer
                    sh 'docker run -i -v "$(pwd)":/workdir -w /workdir -e PHP_CS_FIXER_IGNORE_ENV=1 unibeautify/php-cs-fixer fix -v --dry-run --stop-on-violation --using-cache=no getconfig.php'
                }
            }
        }
    }
}
