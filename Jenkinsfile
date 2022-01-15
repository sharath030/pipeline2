pipeline    {
            agent any
            stages {
             stage('BUILD'){
                steps {
                        git branch: 'main', url :'https://github.com/reddyprashanth305/java-codes.git'
                        sh 'mvn clean install'
                    }
                  }
                  stage('DEPLOY') {
                   steps {
                        sh 'scp -r /var/lib/jenkins/workspace/pipelinejob/target/hello-world-war-1.0.0.war/ ec2-user@172.31.46.19:/home/ec2-user/'
             	 }
				     }
			        	stage('STATUS') {
					      steps {
						      sh 'echo "java file build in one slave & deploy in other slave using pipeline successfully completed"'	
					}
				}
			}
		}
