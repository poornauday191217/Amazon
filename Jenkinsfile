pipeline {    
    agent any   
    stages {
        stage('git clone'){
            steps{
                git branch: 'master' ,url: 'https://github.com/poornauday191217/Amazon'
            }
        }
        stage('build'){
            steps{
                sh 'mvn clean install'
            }
        }
    }
    post{
        //always{
         //   deleteDir() 
        //}
        success{          
           // mail to: 'poornavenkatalaxmi@gmail.com', 
           //        subject: 'Pipeline build is over, build # is ${env.BUILD_NUMBER} and build status is ${currentBuild.result}', 
          //         body: 'build and deployment was successful' 
           // mail to: 'searchforpoorna@gmail.com', 
           //        subject: 'Pipeline build is over, build # is ${env.BUILD_NUMBER} and build status is ${currentBuild.result}', 
           //        body: 'build and deployment was successful' 
           echo "Build over"
            
        }
        failure{
            echo "Failed"
        }
    }
}

