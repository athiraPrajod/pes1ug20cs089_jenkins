pipeline
{
    agent any
    stages
    {
        stage ('Build')
        {
            steps
            {
                sh 'g++ task5.cpp'
                echo 'build stage successful'
                build job: 'pes1ug20cs089'
            }
        }
        stage ('Test')
        {
            steps
            {
                sh './a.out'
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
