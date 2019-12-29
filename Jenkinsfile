pipeline {
    agent any
    stages{
        stage('Clean'){
	    steps {
		sh 'mvn clean'
		 }
	 }
	 stage('validate'){
	   steps {
		sh 'mvn validate'
		}
	}
	 stage('Test'){
	   steps {
		sh 'mvn test'
		}
	}
        stage('Do you want to proceed..?') {
                 steps {
                    input('Do you want to proceed?')
                 }
                 }
	 stage('Package'){
		steps {
			sh 'mvn package'
			}
		}
	 stage('verify'){
		steps {
			sh 'mvn verify'
		}
	}
	 stage('install'){
		steps {
			sh 'mvn install'
		}
                }
}
}
