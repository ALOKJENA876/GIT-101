pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                bat 'echo %path%'
                bat 'python -m py_compile add2vals.py calc.py' 
                stash(name: 'compiled-results', includes: '*.py*') 
            }
        }
    }
}