pipeline{
    agent{lable: 'master'}
    tools{maven: 'M3'}
    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/Sakshibobde/SpringPetClinic.git'
            }
        }
        stage('build'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('deploy'){
            steps{
                sh 'java -jar /var/lib/jenkins/workspace/PetClinicPipline/target/*.jar'
            }
        }
    }
}
