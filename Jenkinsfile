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
		
		/*stage ('Build') {
            steps {
               script{
						sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml "
				    }
            }
        }*/
		
		stage ('docker') {
            steps {
               script{
						sh "ansible-playbook ansible/docker.yml -i ansible/inventory/host.yml "
				    }
            }
        }

    }
   
    
    
}
