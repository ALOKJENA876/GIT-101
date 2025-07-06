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
        stage('Test') {
            steps {
                 bat 'echo Fix later'
                //bat 'python -m pytest --junit-xml test-reports/results.xml test_calc.py'
            }
            post {
                always {
                    bat 'echo Fix later'
                   // junit 'test-reports/results.xml'
                }
            }
        }
        stage('Deliver') {
            steps {
                bat 'echo Fix later'
                //bat "python -m PyInstaller --onefile add2vals.py"
            }
            post {
                success {
                    bat 'echo Fix later'
                    //archiveArtifacts 'dist/add2vals'
                }
            }
        }
    }
}