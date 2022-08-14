pipeline {
    agent any

    stages {
        stage('Time') {
            steps {
                
                script{
                    def now = new Date()
                    def times = now.format("yyMMdd.HHmm", TimeZone.getTimeZone('UTC'))
                    def slackResponse = slackSend(channel: "#pollachi-cbe", message: "Hello, this is created from build pipleine")
                    slackSend(channel: slackResponse.channelId, message: "${times}", timestamp: slackResponse.ts)  
        
                }
            }
        }
    }
}

