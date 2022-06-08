pipeline {

    agent any
        options{
               office365ConnectorSend (
    status: "Pipeline Status",
    webhookUrl: "https://automationanywhere1.webhook.office.com/webhookb2/270476cd-c12b-441c-bea4-f23efe029187@f03022ed-34ea-4c8f-91cb-9abee0a20907/IncomingWebhook/a4229773c440496394ebedf498121199/1d452f31-e9db-45c5-85b8-a0d2b62b1adf",
    color: '00ff00',
    message: "Job started: ${JOB_NAME} - ${BUILD_DISPLAY_NAME}<br>Pipeline duration: ${currentBuild.durationString}"
  )
  }

    stages {
        stage('Init') {
            steps {
                echo 'Starting!'
                office365ConnectorSend message: 'Approval needed', webhookUrl: 'https://automationanywhere1.webhook.office.com/webhookb2/270476cd-c12b-441c-bea4-f23efe029187@f03022ed-34ea-4c8f-91cb-9abee0a20907/IncomingWebhook/a4229773c440496394ebedf498121199/1d452f31-e9db-45c5-85b8-a0d2b62b1adf'
            }
        }
    }
}
