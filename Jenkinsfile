pipeline {
  agent any
  stages {
    stage ('First') {
      steps {
          echo "inside steps"
      
      
          script {
            
            def poUser = getConsumer 'Pipeline Object User'
            def hey = helloWorld 'Object to be Used'
          
            poUser.consumeResponseContent(hey)
            
            def passedObject = poUser.getConsumedObject()
            
            echo poUser.getGreeting()
            echo passedObject.getGreeting()
        }
      }
    }
  }
}
