pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                bat 'echo %path%'
                bat 'python -m py_compile add2vals.py calc.py' 
                bat 'python add2vals.py 5 10'
                stash(name: 'compiled-results', includes: '*.py*') 
            }
        }
    }
}