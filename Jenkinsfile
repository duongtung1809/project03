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
			git branch: 'main', credentialsId: 'github-id', url: 'https://github.com/duongtung1809/project03.git'
			sh 'git config --global user.name "tung"'
                        
			sh 'git config --global user.email "tungdt1809@gmail.com"'
			sh 'git commit -m "changed README" '
			//sh 'git push origin main'
		
		}
            }
        }
    }
}
