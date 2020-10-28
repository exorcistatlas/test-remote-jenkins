pipeline {
   agent any
   stages {
    stage('Clone git') {
      steps {
        script {
           // The below will clone your repo and will be checked out to master branch by default.
           git credentialsId: '080380d6-566f-4e59-969c-623550278171', url: 'https://github.com/exorcistatlas/test-remote-jenkins.git'
           // Do a ls -lart to view all the files are cloned. It will be clonned. This is just for you to be sure about it.
           sh "ls -lart ./*" 
           sh "ansible-playbook playbook.yml"
           // List all branches in your repo. 
           // sh "git branch -a"
           // Checkout to a specific branch in your repo.
           // sh "git checkout branchname"
          }
       }
    }
  }
}
