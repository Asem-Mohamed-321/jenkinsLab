@Library('shared-library')_
pipeline {
    agent {
        label 'default'
        
    }
    stages{
        stage (DockerBuild){
        steps{
                                 buildDockerImage("newlab")  
            }
        }

        stage(Dockerpush){
            steps{
                                pushDockerImage("newlab")
            }
        }

        stage(OpenshiftDeployment){
            steps{
                                openshiftDeployment("asemmohamed321/newlab")
            }
        }
    }
    
}
