pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                // Get some code from a GitHub repository
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/adarshss27/jenkins_ansible_test.git']]])
                sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'ansible-playbook /home/adarsh/project15/dir1/gather_fact.yml' ,execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: 'project15/dir1', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '/*')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
            
        }
    }
}
