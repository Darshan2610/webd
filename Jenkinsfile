pipeline{
    agent any
    tools{
        maven 'maven'
        
    }
    
    stages{
        stage('checkout'){
            steps{git 'https://github.com/Darshan2610/webd.git'}
        }
    
    
    stage('build'){
        steps{
            sh 'mvn clean package'
        }
    }
    
    stage('archive'){
        steps{
            archiveArtifacts artifacts: 'target/*.war', fingerprint:true
        }
    }
    
    stage("deploy"){
        steps{
            ansiblePlaybook playbook:'ansible/deploy.yml', inventory:'ansible/hosts.ini'
        }
    }
    
    }
    

}
