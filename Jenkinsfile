pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                bat 'C:\Users\jenaa\AppData\Local\Microsoft\WindowsApps\python.exe -m py_compile add2vals.py calc.py' 
                stash(name: 'compiled-results', includes: '*.py*') 
            }
        }
    }
}