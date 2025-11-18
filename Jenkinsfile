pipeline {
agent any
environment {
DOCKER_USER = 'poste06dockerpassword'
}
stages {
stage('Login Docker') {
steps {
withCredentials([string(credentialsId: 'DOCKER_PASSWORD', variable: 'POSTE06-DOCKER_PASS')]) {
sh 'echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin'
}
}
}
}
}
