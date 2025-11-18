pipeline{
    agent any
    environment{
        python="C:\\Users\\Subhra\\AppData\\Local\\Programs\\Python\\Python314\\python.exe"

    }
    stages{
        stage("checkout"){
            steps{
                checkout scm
            }
        }
        stage("requirements"){
            steps{
                bat """
                ${python} -m pip install -r requirements.txt
                """
            }
        }
        stage("extract data"){
            steps{
                bat "${python} extract.py"
            }
        }
    }

}