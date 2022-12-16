pipeline {
    agent any
    
    tools {
        nodejs 'node16.16.0'
    }
    

    stages {
        stage('SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/amal703/react-todo-app.git'

            }
        }
        stage('npm install') {
            steps {
               sh 'npm install'
            
            }
        }

        stage('build') {
            steps {
                
             sh'''
             npm rebuild node-sass
             npx browserslist@latest --update-db 
             npm run build
              '''
            }
        }
        stage('deploy') {
        steps {
            sh 'cp -R build/* /var/www/html/' 
           }
        }
     }
}
