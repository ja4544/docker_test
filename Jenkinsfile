node {
   stage('Preparation') {
      git (
        poll: true,
        url: 'https://github.com/ja4544/docker_test.git'
      )
   }
   stage('Test') {
     echo "${WORKSPACE}"
     //scriptFile = getClass().protectionDomain.codeSource.location.path
     //echo scriptFile
     sh 'cd /Users/ja4544/projects/jenkins && source ./venv/bin/activate && tox'
   }
   stage('Build') {
     sh 'cd /Users/ja4544/projects/jenkins && docker-compose up -d --build'
   }
}
