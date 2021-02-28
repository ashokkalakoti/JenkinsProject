pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Hello CloudBabies!!!"'
        sh '''
                    echo "Welcome to Jenkins..."
                    echo "This is the new line in jenkins file"
                    echo "This is the 3rd line of jenkins file"
                    ls -lah
                '''
      }
    }

    stage('wait for confirm') {
      steps {
        timeout(time:1, unit:"DAYS") {
          input(message: 'Deploy to Prod?', ok: 'Yes Let\'s do it.!')
      }
    }

  }
}
