node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t josiah:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'lornanyokabi' -p 'Nairobi12345' "
sh "docker tag josiah:latest lornanyokabi/josiah:latest"
sh "docker push lornanyokabi/josiah:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
