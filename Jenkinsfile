pipeline{
	agent {label 'slave1'}
		stages {
			stage('Preperation'){
				steps{ sh 'docker pull ubuntu'
				       sh 'docker pull nginx'
					}
				}
			stage('build'){
				steps{ sh 'docker run -itd ubuntu'
					}
				}
			stage('test'){
				steps{ echo 'this is testing stage'
					}
				}
			stage('deploy'){
				steps{ input ('Do you want to proceed?')
					echo 'this is deploy stage'
					}
				}
	}
}

