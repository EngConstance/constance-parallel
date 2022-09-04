pipeline{
	agent any 
	stages{
		stage('git-clone2'){
			steps{
				checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/EngConstance/constance-parallel.git']]])
			 
			}
		}
		stage('parallel-level'){
			prallel {
				stage('sub-job1'){
					steps{
						echo "sub-job1task"
					}
				}
				stage('sub job2'){
					steps{
						echo "sub-job2 task"
					}
				}
			}
		}
		stage('version-check'){
			steps{
				echo "end of parallel job"
			}
		}
		
	}
}
