pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                // checkout([$class: 'GitSCM', branches: [[name: '*/main/']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/adarshss27/jenkins_ansible_test.git']]])               
                git 'https://github.com/adarshss27/jenkins_ansible_test.git'
                sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible', transfers: [sshTransfer(cleanRemote: false, excludes: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: 'pro1', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '*')])
            } 
        }
    }
}
