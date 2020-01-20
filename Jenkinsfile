node {
  try {
    stage('Clone') {
      git url: 'https://github.com/ekhv/demo.git'
    }

    stage('Deploy'){
        sh 'docker build -t node-app --no-cache .'
        sh 'docker tag node-app localhost:5000/node-app'
    }
    
    stage('Test'){
        sh 'docker run --name node-app echo "curl -s http://localhost:49160/"'
    }
  }
  catch (err) {
    throw err
  }
}
