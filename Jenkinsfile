pipeline {
  agent {
    docker {
      image 'maven:3.8.4-openjdk-11-slim'
    }
  }
  stages {
    stage('2183322c-Stage1') {
      steps {
        echo "Start of Pipeline - 2183322c Stage 1 Completed"
      }

    }
    stage('2183322c-Stage2') {

      steps {
        echo "Email Triggered - 2183322c Stage 2 Completed"
      }
    }
    stage('2183322c-Stage3') {
      steps {
        docker run - d--name 218332 c - test - t 2183322 c - image
        echo "Application Setup - 2183322c Stage 3 Completed"
      }
    }
    stage('2183322c-Stage4') {
      steps {
        parallel(
          '2183322c-Test1': {
            echo "App Test 1 Success - 2183322c Stage 4C Completed"
          },
          '2183322c-Test2': {
            echo "App Test 1 Success - 2183322c Stage 4B Completed"
          }
        )
      }
    }
    stage('2183322c-Stage5') {
      steps {
        script {
          env.PROCEED = input message: 'Proceed to release the work to Prod Env ?'
        }
        echo "Proceed to release the work to Prod Env ?"
      }
    }
    stage('2183322c-Stage6') {
      steps {
        if ($ {
            env.USERNAME
          } == 'PROCEED') {
          echo "2183322c - Work Releases to Prod Env"
        } else {
          Abort
        }
      }

    }
  }
}
