pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'clone git..'
                script {
                    	git 'https://github.com/duongtung1809/project03.git'                    
                }
            }
        }
        stage('Change') {
            steps {
                echo 'modify data..'
		script{
			sh '''cd project03/ 
			cat >> README.md << "EOF"
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
