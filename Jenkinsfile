node{
    stage('download') {
     git branch: 'master', url: 'https://github.com/srilatha71/java-war-project-latest-working.git'
}  
        stage('build') {
     sh 'mvn clean package'
}

stage('ContinuousDeployment')
    {
        input message: 'Waiting for Approval from the DM', submitter: 'admin'
        sh label: '', script: 'scp /var/lib/jenkins/workspace/ci-cd-pipeline/target/my-app.war ubuntu@172.31.93.244:/opt/tomcat/webapps/prodenv.war'
    }

}
