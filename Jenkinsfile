node {
    docker.image('node:16-buster-slim').inside('-p 3000:3000') {
        stage('Prepare') {
            sh 'npm cache clean –force'
            sh 'npm rm -rf node_modules && rm package-lock.json'
        }
        stage('Build') {
                sh 'npm install'
            }
        stage('Test') { 
                sh './var/jenkins_home/workspace/react-app/jenkins/scripts/test.sh' 
        }
    }
}
