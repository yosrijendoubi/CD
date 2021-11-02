pipeline {

    agent any


    stages {
       stage ('Pull') {
            steps {
               script{
						checkout([$class: 'GitSCM',
     branches: [[name: "*/master" ]],
     userRemoteConfigs: [[credentialsId: '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', url: 'https://github.com/yosrijendoubi/CD.git']]
         ])
				    }
            }
        }

    }
   
    
    
}
