node {
  try {
    stage('Clone') {
      git url: 'https://github.com/ekhv/demo.git'
    }

    stage('Deploy'){
        sh 'docker build -t node-app --no-cache .'
        sh 'docker tag node-app localhost:5000/node-app'
    }
  }
  catch (err) {
    throw err
  }
}
