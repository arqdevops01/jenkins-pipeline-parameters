pipeline {
    agent any

    parameters {
        string(name: 'NUMBER1', defaultValue: '0', description: 'First number to add')
        string(name: 'NUMBER2', defaultValue: '0', description: 'Second number to add')
    }

    stages {
        stage('BuildExecute') {
            steps {
                echo 'Build and execute python'
                // Set up Python environment (optional)
                //sh 'python3 -m venv venv'
                //#sh '. venv/bin/activate'

                // Set up python enviroment MINICONDA
                sh '''eval "$(/var/jenkins_home/miniconda3/condabin/conda shell.bash hook)" 
                      conda activate PythonJenkins
                      python3 sum.py "${params.NUMBER1} ${params.NUMBER2}"'''
                

            }
        }
        
    }    
}
