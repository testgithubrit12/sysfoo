pipeline{
    agent { label 'slave-2' }
    tools{
        maven 'Maven 3.8.6'
    }
    stages{
        stage('Compile'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                sh 'mvn clean test'
            }
        }
        stage('package'){
            steps{
                sh 'mvn package -DskipTests'
            }
        }
    }
}
post{
  always {
     echo "This block always runs."
  }
}
