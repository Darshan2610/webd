pipeline{
    agent any
    tools{
        maven 'maven'
        
    }
    
    stages{
        stage('checkout'){
            steps{git 'https://github.com/Darshan2610/webd.git'}
        }
    }
    
    stage(''build){
        steps{
            sh 'mvn clean package'
        }
    }
    

}
