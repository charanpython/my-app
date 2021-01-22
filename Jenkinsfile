node{

stage("Pulling code fro GIT"){
    git 'https://github.com/charanpython/my-app'
}

stage("Compile and Package"){
    //GET MVN HOME PATH
    def mvnHOME = tool name: 'mven-3.6', type: 'maven'
    sh "${mvnHOME}/bin/mvn package"
}
    
    stage('Deploying'){
    
        sshagent(['tomcat-dev']) {
        sh 'scp -o StrictHostKeyChecking=no target/*.war ec2-user@172.31.16.220:/opt/apache-tomcat-9.0.41/webapps/'
}
    }
    
    
}
