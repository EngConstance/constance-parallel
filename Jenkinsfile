pipeline{
	agent any 
	stages{
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
