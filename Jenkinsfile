podTemplate(
containers: [
    containerTemplate(
        name: 'jnlp',
        image: 'jenkinsci/jnlp-slave:2.62',
        command: '',
        args: '${computer.jnlpmac} ${computer.name}',
        envVars: [
            envVar(key: 'JENKINS_URL', value: 'http://cs-jenkins-jenkins:8080')
        ],
        workingDir: '/home/jenkins'
    )
], label: 'cs-go') {

    node('cs-go') {
        echo 'Hello world'
        sleep params.SLEEP.toInteger()
    }

}
