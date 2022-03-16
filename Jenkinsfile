pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable. agent notify which jenkins instance is being used
    tools{
       nodejs 'nodejs' 
    }
   

    stages{
        stage('compile'){
            steps{
                echo 'this is the first job compile'
                sh 'npm install'
                //sleep 4
            }
        }
        stage('test'){
            steps{
                echo 'this is the second job test'
                sh 'npm test'
                //sleep 9
            }
        }
		
        stage('package'){
            steps{
                echo 'this is the third job package'
                sh 'npm run package'
                //sleep 7
            }
        }
    }
    
    post{
        always{
            echo 'this is first pipeline by code...'
        }
        
    }
    
}
