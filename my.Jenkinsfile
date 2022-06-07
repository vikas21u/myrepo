pipeline {

    agent any

    options {
        office365ConnectorWebhooks([[
                    startNotification: true,
                        url: 'https://outlook.office.com/webhook/123456...'
            ]]
        )
    }

    stages {
        stage('build') {
            steps {
                echo 'Hello'
            }
        }
    }
}