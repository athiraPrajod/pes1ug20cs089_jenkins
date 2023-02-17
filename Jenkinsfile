pipeline
{
    agent any
    stages
    {
        stage ('Build')
        {
            steps
            {
                sh 'make main/'
                echo 'build stage successful'
                build job: 'pes1ug20cs089'
            }
        }
        stage ('Test')
        {
            steps
            {
                sh './hello_exec'
                echo 'test stage successful'
            }
        }
        stage ('Deploy')
        {
            steps
            {
                echo 'Deployment successful'
            }
        }
    }
    post
    {
        failure
        {
            echo 'Pipeline failed'
        }
    }
}
