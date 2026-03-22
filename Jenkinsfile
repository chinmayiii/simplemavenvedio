pipeline{
agent any
  tools{
    maven 'Maven'
  }
  stages{
    stage('Checkout'){
      steps{
        git branch:'main',url:'
      }
    }
    stage('Build'){
      steps{
        sh 'mvn clean package'
      }
    }
    stage('Test'){
      steps{
        sh 'mvn test'
      }
    }
    stage('Run Application'){
      steps{
        sh 'java -jar target/
      }
    }
  }
  post{
    success{
      echo 'Build and deployment succesfull'
    }
    failure{
      echo 'Build failed'
    }
  }
}
