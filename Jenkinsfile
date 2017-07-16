pipeline{

  agent any

  stages{
        stage('Build Project'){

            steps{

            echo 'Building the Project.....'
            sh 'ant -f build.xml -v'


            }
        }

        stage('Test Project'){

            steps{

            echo 'Testing the Project ....'

            }
        }

        stage('Deploy Project'){

            steps{

            echo 'Deploying the project ....'


            }

        }

  }


  post {

        always{
            echo 'Archiving the files .......'
            archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true

        }

  }


}
