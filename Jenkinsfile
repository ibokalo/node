node {
    stage('Clone repository') {
        git branch: "master", url: "git@gitlab.s-pro.io:ibokalo/backend.git", credentialsId: "jenkins-gitlab"
    }
    stage('Build image') {
        sh "docker build -t 907208926079.dkr.ecr.eu-central-1.amazonaws.com/modoenergy/back-dev-v2 --no-cache -f Dockerfile-dev ."
        sh "docker tag modoenergy/back-dev-2:latest 907208926079.dkr.ecr.eu-central-1.amazonaws.com/modoenergy/back-dev-2:latest"
    }
    stage('Push image') {
        docker.withRegistry('https://907208926079.dkr.ecr.eu-central-1.amazonaws.com/modoenergy/back-dev-v2') {
            sh "docker push 907208926079.dkr.ecr.eu-central-1.amazonaws.com/modoenergy/back-dev-v2:latest"
        }
    }
}