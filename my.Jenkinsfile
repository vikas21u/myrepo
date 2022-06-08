pipeline {

    agent any

    options {
        office365ConnectorWebhooks([[
                    startNotification: true,
                    notifySuccess: true,
                    factDefinitions: [[name: "Environment", template: "${environment}"],
                                     [name: "fact2", template: "content of fact2"]],
                        url: 'https://automationanywhere1.webhook.office.com/webhookb2/270476cd-c12b-441c-bea4-f23efe029187@f03022ed-34ea-4c8f-91cb-9abee0a20907/IncomingWebhook/a4229773c440496394ebedf498121199/1d452f31-e9db-45c5-85b8-a0d2b62b1adf'
    }

    stages {
        stage('Approval') {
            steps {
                office365ConnectorSend webhookUrl: 'https://automationanywhere1.webhook.office.com/webhookb2/270476cd-c12b-441c-bea4-f23efe029187@f03022ed-34ea-4c8f-91cb-9abee0a20907/IncomingWebhook/a4229773c440496394ebedf498121199/1d452f31-e9db-45c5-85b8-a0d2b62b1adf',
                message: 'Approval needed',
                echo 'Hello'
            }
        }
    }
}
