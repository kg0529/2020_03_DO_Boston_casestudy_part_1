pipeline{
	agent any	
	environment {
		REGISTRY_CREDENTIAL = "dockerhub"
	}
	stages{
		stage('check-out'){
			steps{
				sh 'rm -rf 2020_03_DO_Boston_casestudy_part_1'
				sh 'git clone https://github.com/kg0529/2020_03_DO_Boston_casestudy_part_1.git'
			}
		}
		stage('Deploy'){
			steps{
				script {
					sh 'ansible-playbook flask-playbook.yml'
				}
			}
		}
	}
}
