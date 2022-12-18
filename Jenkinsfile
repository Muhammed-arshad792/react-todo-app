pipeline {
	agent any 
	tools {
	nodejs "node16.16.0"}

	stages  {

	    stage('Source Code Management') {
	        steps {
	            git branch: 'main', url: 'https://github.com/Muhammed-arshad792/react-todo-app.git'
	        }
	    }
	    stage('npm install') {
	        steps {
	            sh 'npm install'
	        }
	    }
	    stage('build') {
	        steps {
	        sh 'npm install --save react-router-dom'
	        sh 'npm run build'
	        }
	    }
	    stage('Deploy') {
	        steps {
	        sh 'cp -rv  /var/lib/jenkins/workspace/react_todo/build/*   /var/www/html/'
	        }
	    }
	}
}
