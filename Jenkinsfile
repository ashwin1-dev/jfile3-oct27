pipeline {
	agent any

        tools {
		maven "jenkin-maven"
              }


        stages {
		stage('build') {
			steps {
				git 'https://github.com/ashwin1-dev/maven-jar-oct27.git'
				sh "mvn clean install"
				sh "scp /var/lib/jenkins/workspace/pipe/target/.war  192.168.10.32:/opt/tomcat/webapps"

				}
			     }
   	}
}
