pipeline{
agents any
stages {
    stage ('Compile Stage')
    {
        steps{
        withMaven(maven :'M3')
        {
            sh 'mvn clean compile'
        }
        }

    }
    stage ('Testing stage')
    {
        steps{
            withMaven(maven :'M3')
                    {
                        sh 'mvn test'
                    }
        }
    }
    stage ('Deployment stage')
        {
            steps{
                withMaven(maven :'M3')
                        {
                            sh 'mvn deploy'
                        }
            }
        }


}


}
