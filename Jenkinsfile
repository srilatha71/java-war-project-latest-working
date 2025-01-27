node{
    stage('download') {
     git branch: 'master', url: 'https://github.com/srilatha71/java-war-project-latest-working.git'
}  
        stage('build') {
     sh 'mvn package'
}

stage('ContinuousDeployment')
    {
        input message: 'Waiting for Approval from the DM', submitter: 'admin'
        sh label: '', script: 'cp /var/lib/jenkins/workspace/pipeline/target/my-app.war /opt/tomcat/updated/webapps/testenv.war'
    }

}
