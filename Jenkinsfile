pipeline {
    agent any

    tools {
        gradle 'Gradle'
    }

    stages {
        stage("run frontend"){
            steps{
                echo "executing yarn"
                nodejs('NodeJs') {
                    sh 'yarn install'
                }
            }
        }
        stage("run backend"){
            steps{
                echo "executing gradle"
                withGradle(){
                    sh 'echo Gradle nhu lon'
                }
            }
        }
    }
}