pipeline {
    agent { node { label 'workstation' } }

    parameters {
            string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

            text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

            booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

            choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

            password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                script {
                  withAWSParameterStore(credentialsId: 'AWS', naming: 'absolute', path: '/dev', recursive: true, regionName: 'us-east-1') {
                    sh 'env'
                  }
                }
            }
        }
    }
}
