post {
      always {
        cleanWs()
      }
      failure {
          slackSend baseUrl: 'https://hooks.slack.com/services/',
          channel: '#build-failures',
          iconEmoji: '',
          message: "CI failing for - #${env.BRANCH_NAME} - ${currentBuild.currentResult}  (<${env.BUILD_URL}|Open>)",
          teamDomain: 'differentau',
          tokenCredentialId: 'slack-token-build-failures',
          username: ''
        }
    }
