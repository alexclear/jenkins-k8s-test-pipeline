stage("A sample step") {
    podTemplate(label: 'kubernetes',
                        containers: [containerTemplate(name: 'cloudbees-jnlp-slave',
                        image: 'cloudbees/jnlp-slave-with-java-build-tools:latest',
                        ttyEnabled: true)]
    ) {
        node("kubernetes") {
            container("cloudbees-jnlp-slave") {
                sh "ls -alF /"
            }
        }
    }
}
