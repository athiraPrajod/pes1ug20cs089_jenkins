pipeline
{
    agent any
    stages
    {
        stage ('Build')
        {
            steps
            {
                sh 'g++ -o task5 task5.cpp'
                echo 'build stage successful'
                build job: 'pes1ug20cs089'
            }
        }
        stage ('Test')
        {
            steps
            {
                sh './task5'
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
