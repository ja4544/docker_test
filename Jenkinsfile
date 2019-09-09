node {
   stage('Preparation') {
      git (
        poll: true,
        url: 'https://github.com/ja4544/docker_test.git'
      )
   }
   stage('Test') {
     sh 'pwd'
     sh 'cd /Users/ja4544/projects/jenkins && source ./venv/bin/activate && tox'
   }
   stage('Build') {
     sh 'cd /Users/ja4544/projects/jenkins && docker-compose up -d --build'
   }
}
