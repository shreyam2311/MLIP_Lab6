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

                # Use the specific path to Conda to initialize (if needed) and run commands
                # Initialize Conda - may not be necessary for non-interactive shell scripts
                # /home/team17/miniconda3/bin/conda init bash

                # Run pytest using the 'mlip' Conda environment
                /home/team17/miniconda3/bin/conda run -n mlip pytest

                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our project'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}