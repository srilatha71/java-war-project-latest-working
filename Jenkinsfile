node('node-1'){
    stage('download') {
     git url: 'https://github.com/srilatha71/java-war-project-latest-working.git'
}  
        stage('build') {
     sh 'mvn clean package'
}

stage('ContinuousDeployment')
    {
        input message: 'Waiting for Approval from the DM', submitter: 'admin'
        sh label: '', script: 'cp /opt/tomcat/jenkins/workspace/multi-Branch_develop/target/my-app.war /opt/tomcat/updated/webapps/devenv.war'
    }

}
