//pipeline {
//    agent { node { label 'workstation' } }
//
//    parameters {
//            string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//
//            text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
//
//            booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
//
//            choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
//
//            password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
//    }
//
//    stages {
//        stage('Hello') {
//            steps {
//                echo 'Hello World'
//                script {
//                  withAWSParameterStore(credentialsId: 'AWS', naming: 'absolute', path: '/dev', recursive: true, regionName: 'us-east-1') {
//                    sh 'env'
//                  }
//                }
//            }
//        }
//    }
//}
//
//
//pipeline {
//    agent any
//    stages {
//        stage('Example') {
//            input {
//                message "Should we continue?"
//                ok "Yes, we should."
//                submitter "admin"
//                parameters {
//                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//                }
//            }
//            steps {
//                echo "Hello, ${PERSON}, nice to meet you."
//            }
//        }
//    }
//}


pipeline {
    agent any
    stages {
        stage('Stage1') {
            when {
                expression { BRANCH_NAME ==~ /(production|staging)/ }
            }
            steps {
                echo 'Deploying'
            }
        }

        stage('Stage2') {

            steps {
                echo 'Deploying'
            }
        }

    }
}

