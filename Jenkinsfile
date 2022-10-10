pipeline {
  agent any
  stages {
    stage('Install Apache') {
      steps {
        sh 'sudo apt install apche2 -y'
      }
    }

    stage('Fetch Code') {
      steps {
        git(url: 'https://github.com/rahul17111996/blueocean.git', branch: 'main', poll: true)
      }
    }

    stage('Deploy') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}