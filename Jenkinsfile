node {
    stage ('scm checkout'){
       git credentialsId: 'github_creds', url: 'https://github.com/kunchamrajkumar/my-app.git' 
    }
    stage ('mvn package'){
        sh 'mvn  clean package'
    }
    stage ('build docker image'){
        sh 'docker build -t tomcat:jre11-temurin .'
    }
}
