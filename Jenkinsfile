node{

stage("Pulling code fro GIT"){
    git 'https://github.com/charanpython/my-app'
}

stage("Compile and Package"){
    //GET MVN HOME PATH
    def mvnHOME = tool name: 'Maven3.6', type: 'maven'
    sh '${mvnHOME}/bin/mvn package'
}



}
