pipeline{
	agent { label 'slave-2'}
	stages{
        stage('Build stage') {
            steps {
                echo 'This is a build stage'
				sh 'sleep 5'
			}
		}
        stage('Push stage') {
            steps {
                echo 'This is push stage'
                sh 'sleep 5'
			}
		}
        stage('Deploy stage') {
            steps {
                echo 'This is deploy stage'
                sh 'sleep 5'
			}
		}
		stage('test stage') {
			parallel (
				stage('test1'){
				steps{
					echo 'this is test1'
				}
				}
				stage('test2') {
					steps{
						echo 'this is test2'
					}
				}
				)
		}
	}
}	
