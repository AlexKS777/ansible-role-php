stage('testing webhook') {

    node('master') {

        checkout scm
        sh 'echo  triggered webhook'
        githubNotify repo: 'ansible-role-php', credentialsId: 'c5a8aa55-c690-4b53-892e-b427f232f668', description: 'triggered webhook', context: "Stage I",  status: 'PENDING'
        sh 'sleep 15'
        sh 'echo build finished'
        githubNotify repo: 'ansible-role-php', credentialsId: 'c5a8aa55-c690-4b53-892e-b427f232f668', description: 'build finished', context: "Stage I",  status: 'SUCCESS'
    }
}

stage('testing webhook - stage II') {

    node('master') {

        checkout scm
        sh 'echo  triggered webhook - stage II'
        githubNotify  credentialsId: 'c5a8aa55-c690-4b53-892e-b427f232f668', description: 'triggered webhook - stage II', context: "Stage II",  status: 'PENDING'
        sh 'sleep 15'
        sh 'echo build finished - stage II'
        githubNotify credentialsId: 'c5a8aa55-c690-4b53-892e-b427f232f668', description: 'build finished - stage II', context: "Stage II",  status: 'SUCCESS'
    }
}
