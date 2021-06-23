pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                // Get some code from a GitHub repository
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/adarshss27/jenkins_ansible_test.git']]])
                sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'echo "hello"', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: 'pro/dir1', remoteDirectorySDF: false, removePrefix: '', sourceFiles: 'main/dir1'), sshTransfer(cleanRemote: false, excludes: '', execCommand: 'echo "hi"', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: 'pro1/dir2', remoteDirectorySDF: false, removePrefix: '', sourceFiles: 'main/dir2')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            } 
        }
    }
}
