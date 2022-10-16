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
			sh 'git config --global user.name "tung"'
			sh 'git config --global user.email "tungdt1809@gmail.com"'
			sh 'git add .'
			sh 'git commit -m "changed README"'
			sh 'git remote add origin https://github.com/duongtung1809/project03.git'
			
		}
            }
        }
        stage('Push') {
            steps {
		withCredentials([usernamePassword(credentialsId: 'github-id', usernameVariable: 'username',passwordVariable: 'password')]){
               		sh 'git push http://$username:$password@github.com:duongtung1809/project03.git'
		
		
            }
        }
    }
}
