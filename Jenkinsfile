pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
/*    tools{
       maven 'maven' 
    }
*/    

    stages{
        stage('Build'){
            steps{
                echo 'this is the build job'
                sh 'mvn compile'
            }
        }
        stage('Test'){
            steps{
                echo 'this is the test job'
                sh 'mvn clean test'
            }
        }
        stage('Package'){
            steps{
                echo 'this is the package job'
                sh 'mvn package -DskipTests'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
