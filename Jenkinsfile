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
			sh 'git add README.md'
			sh 'git commit -m "changed README" '
			sh 'git push origin main'
			sh 'tungdt1809@gmail.com'
			sh 'tung18092000'
		}
            }
        }
    }
}
