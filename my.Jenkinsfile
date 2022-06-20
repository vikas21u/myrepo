pipeline {

    agent any
        options {
            configure {
            // Example: Conditioning webhook trigger on build parameter 'version' being equal to 'latest'
            // Templates are defined as token macros https://github.com/jenkinsci/token-macro-plugin
            it / 'properties' / 'jenkins.plugins.office365connector.WebhookJobProperty' / 'webhooks' / 'jenkins.plugins.office365connector.Webhook' / 'macros' << 'jenkins.plugins.office365connector.model.Macro' {
            template('${ENV, var="version"}')
            value('latest')
            }
        }
    }

    stages {
        stage('Init') {
            steps {
                echo 'Starting!'
                office365ConnectorSend message: 'Approval needed', webhookUrl: 'https://automationanywhere1.webhook.office.com/webhookb2/270476cd-c12b-441c-bea4-f23efe029187@f03022ed-34ea-4c8f-91cb-9abee0a20907/IncomingWebhook/a4229773c440496394ebedf498121199/1d452f31-e9db-45c5-85b8-a0d2b62b1adf'
            }
        }
    }
    post {
        failure {
            office365ConnectorSend webhookUrl: 'https://automationanywhere1.webhook.office.com/webhookb2/270476cd-c12b-441c-bea4-f23efe029187@f03022ed-34ea-4c8f-91cb-9abee0a20907/IncomingWebhook/a4229773c440496394ebedf498121199/1d452f31-e9db-45c5-85b8-a0d2b62b1adf',
            message: 'Application has been [deployed](https://uat.green.biz)',
            status: 'Success'
            }
        }            
}
