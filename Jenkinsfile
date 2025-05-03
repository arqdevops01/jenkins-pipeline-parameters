pipeline {
    agent any

    parameters {
        string(name: 'NUMBER1', defaultValue: '0', description: 'First number to add')
        string(name: 'NUMBER2', defaultValue: '0', description: 'Second number to add')
    }

    stages {
        stage('BuildAndExecute') {
            steps {
                echo 'Build and execute python'
            sh "/var/jenkins_home/miniconda3/envs/PythonJenkins/bin/python sum.py ${params.NUMBER1} ${NUMBER2}"
                    
            }
        }        
    }    
}
