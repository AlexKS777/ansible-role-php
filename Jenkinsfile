stage('testing webhook') {

    node('master') {

        checkout scm
        sh 'echo  triggered webhook'
        githubNotify account: 'AlexKS777', repo: 'ansible-role-php', credentialsId: 'c5a8aa55-c690-4b53-892e-b427f232f668', description: 'triggered webhook',  status: 'PENDING'
        sh 'sleep 30'
        sh 'echo build finished'
        githubNotify account: 'AlexKS777', repo: 'ansible-role-php', credentialsId: 'c5a8aa55-c690-4b53-892e-b427f232f668', description: 'build finished',  status: 'SUCCESS'
    }
}
