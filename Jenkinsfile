pipeline {
    agent any 

    stages {
        stage(SCM) {
            steps {
                git branch: 'main', url: 'https://github.com/amal703/react-todo-app.git'
            }
        }

        stage('npm install') {
          steps {
             sh 'npm install'
            
            }
        }

        stage(build) {
            steps {
                sh 'npm run build'
            }
        }
            
        }
    }
