pipeline {
  agent any
  stages {
    stage ('First') {
      steps {
          def poUser = getConsumer 'Pipeline Object User'
          def hey = helloWorld 'Object to be Used'
          
          poUser.consumeResponseContent(hey)
      }
    }
  }
}
