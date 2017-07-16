pipeline{

  agent any

  options {

     buildDiscarder (logRotator(numToKeepStr: '2', artifactNumToKeepStr: '1' ))

  }

  stages{

          stage('Test Project'){

              steps{

              echo 'Testing the Project ....'



              }
          }
        stage('Build Project'){

            steps{

            echo 'Building the Project.....'
            sh 'ant -f build.xml -v'


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
