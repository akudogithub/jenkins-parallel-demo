pipeline{
	agent any
		stages{
			stage('parallel-stage'){
				parallel{
					stage('sub-job1'){
						steps{
							echo "testing parallel stage"
							echo "this is sub-job1"
						}
					}
					stage('sub-job2'){
						steps{
							echo "this is sub-job2"
							id jenkins
						}
					}
				}
			}
			stage('system-check'){
				steps{
					lscpu
					free -m
				}
			}
			stage('system-analysis'){
				steps{
					lsblk
					free -g
				}
			}
		}
}