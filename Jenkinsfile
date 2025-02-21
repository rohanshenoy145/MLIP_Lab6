pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''#!/bin/bash
                echo 'Test Step: We run testing tool like pytest here'

                # TODO fill out the path to conda here
                source /home/rgshenoy/miniconda3/etc/profile.d/conda.sh
                conda activate mlip

            

                # TODO Complete the command to run pytest
                
                pytest --maxfail=1 --disable-warnings
                # sudo /PATH/TO/CONDA run -n <Envinronment Name> <Command you want to run>

                echo 'pytest  runned'
                #exit 1 #comment this line after implementing Jenkinsfile
                '''

            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our porject'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
