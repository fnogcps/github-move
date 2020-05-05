pipeline {
  agent any
  stages {
    stage('#1') {
      steps {
        fileExists 'composer.json'
        fileExists 'composer.lock'
      }
    }
    stage('#2') {
      steps {
        sh 'composer update && ./vendor/bin/phpunit'
      }
    }
  }
}
