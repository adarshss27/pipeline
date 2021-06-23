pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                // Get some code from a GitHub repository
//                 library identifier: '', retriever: legacySCM([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [[$class: 'SparseCheckoutPaths', sparseCheckoutPaths: [[path: '']]]], userRemoteConfigs: [[url: 'https://github.com/adarshss27/jenkins_ansible_test.git']]])
//                 checkout([$class: 'GitSCM', branches: [[name: '*/main/']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/adarshss27/jenkins_ansible_test.git']]])
//                 library identifier: '', retriever: legacySCM([$class: 'GitSCM', branches: [[name: '*/main/']], extensions: [[$class: 'SparseCheckoutPaths', sparseCheckoutPaths: [[path: 'dir1'], [path: 'dir2']]]], userRemoteConfigs: [[url: 'https://github.com/adarshss27/jenkins_ansible_test.git']]])
                git 'https://github.com/adarshss27/jenkins_ansible_test.git'
                sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible', transfers: [sshTransfer(cleanRemote: false, excludes: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: 'pro1', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '*')])
            } 
        }
    }
}
