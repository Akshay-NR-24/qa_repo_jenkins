pipeline{
agent any;
parameters {
  string defaultValue: 'akshay', name: 'name'
  string defaultValue: '20/11/22', name: 'date'
  string defaultValue: '1.1.2', name: 'version'
  choice choices: ['main','master'], name: 'branch'
  choice choices: ['test','uta','prod'], name: 'deploy'
  string defaultValue: 'https://github.com/Akshay-NR-24/qa_repo_jenkins.git', name: 'git_url'
}
  stages{
    stage('GIT'){
      steps{
        git branch:"${params.branch}",url:"${params.git_url}"
        echo "${version}"
        echo "${params.branch}"
        sh '''
        #!/bin/bash
        echo "${node_labels}"
        echo "${name}"
        echo "${node_labels}"
        echo "${name}"
        '''
      }
    }
  }
}
