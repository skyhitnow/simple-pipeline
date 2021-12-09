pipeline { 
    //agent {node {label 'aliyun_agent'}}
    agent any
    agent{
        docker{
            image 'maven:3.8.1-adoptopenjdk-11'
            label 'my-defined-label'
            args  '-v /tmp:/tmp'
        }
    }
    tools {
        maven 'M3' 
        jdk 'jdk8' 
    }
    stages { 
         stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }
        stage('Build') { 
            steps { 
               echo 'This is a minimal pipeline.' 
            }
        }
    }
}
