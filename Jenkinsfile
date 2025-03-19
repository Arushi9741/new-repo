pipeline{
    agent any
    stages{
        stage('git clone')
        steps{
            git url "https://github.com/Arushi9741/new-repo.git",branch:main
        }

        stage('dependency'){
            steps{
                bat ' ' '
                call venv\\Scripts\\active
                python -m venv venv
                python -m pip install --upgrade pip
                pip install pytest
                ' ' '
            }
        }
        stage('test'){
            steps{
                bat ' ' '
                 call venv\\Scripts\\active
                 pytest testfile.py
                 ' ' '
            }
        }
        stage('deploy'){
            steps{
                bat ' ' '
                 call venv\\Scripts\\active
                 python hello.py
                 ' ' '
            }
        }
    }
}



