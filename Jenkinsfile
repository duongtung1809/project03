pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'clone git..'
                script {
                    	sh 'git pull origin main'                    
                }
            }
        }
        stage('Change') {
            steps {
                echo 'modify data..'
		script{
			sh '''cat >> README.md << EOF
		        changed
			EOF
			'''
			
		}
            }
        }
        stage('Push') {
            steps {
                echo 'git push....'		
		sripts{
			git config --global user.name "tung"
                        git config --global user.email "tungdt1809@gmail.com"
			sh 'git add README.md'
			sh 'git commit -m "changed README" '
			sh 'git push origin main'
		
		}
            }
        }
    }
}
