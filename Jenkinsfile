pipeline {
    agent any
    tools{
        maven 'local maven'
    }
    stages{
        stage ('build'){
            steps{
                echo "开始构建....."
                sh 'mvn clean package'
                sh "/usr/local/bin/docker build . -t tomcatwebapp:${env.BUILD_ID}"
        
            }
        }
    }

  
}