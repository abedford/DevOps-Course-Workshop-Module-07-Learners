pipeline {
    agent any
	
	
	checkout scm
		stage('checkout') {
			 steps {
                checkout scm
            }
        stage('Build') {
			agent {
				docker {
					image 'mcr.microsoft.com/dotnet/sdk:5.'
					reuseNode true	
				}
			}
			steps {
				echo 'Building..'
				sh 'dotnet build'
			}
        }
        stage('Testing C#') {
            steps {
                echo 'Testing C#..'
            }
        }
        stage('Building Typescript') {
            steps {
                echo 'Building Typescript....'
            }
        }
		stage('Testing Typescript') {
            steps {
                echo 'Testing Typescript....'
            }
        }
		stage('Running linter on Typescript') {
            steps {
                echo 'Running linter on Typescript....'
            }
        }
    }
}