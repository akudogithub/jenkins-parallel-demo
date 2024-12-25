pipeline{
	agent any
		stages{
			stage('parallel-stage'){
				parallel{
					stage('sub-job1'){
						steps{
							sh 'echo "testing parallel stage"'
							sh 'echo "this is sub-job1"'
						}
					}
					stage('sub-job2'){
						steps{
							sh 'echo "this is sub-job2"'
							sh 'id jenkins'
						}
					}
				}
			}
			stage('system-check'){
				steps{
					sh 'lscpu'
					sh 'free -m'
				}
			}
			stage('system-analysis'){
				steps{
					sh 'lsblk' 
					sh 'free -g'
				}
			}
		}
}