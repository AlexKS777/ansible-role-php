stage('testing webhook') {

    node('master') {

        checkout scm
        sh 'echo  triggered webhook'
        githubNotify credentialsId: 'c5a8aa55-c690-4b53-892e-b427f232f668', description: 'triggered webhook',  status: 'PENDING'
        sh 'sleep 30'
        sh 'echo build finished'
        githubNotify credentialsId: 'c5a8aa55-c690-4b53-892e-b427f232f668', description: 'build finished',  status: 'SUCCESS'
    }
}
