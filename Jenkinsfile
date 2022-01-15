pipeline    {
            agent any
            stages {
             stage('BUILD'){
                steps {
                        git branch: 'main', url :'https://github.com/sharath030/javaproject.git'
                        sh 'mvn clean install'
                    }
                  }
                  stage('DEPLOY') {
                   steps {
                        sh 'scp -r /var/lib/jenkins/workspace/pipelinejob/target/java-noob-1.0.0-SNAPSHOT.jar/ ec2-user@172.31.9.164:/home/ec2-user/'
             	 }
				     }
			        	stage('STATUS') {
					      steps {
						      sh 'echo "java file build in one slave & deploy in other slave using pipeline successfully completed"'	
					}
				}
			}
		}
