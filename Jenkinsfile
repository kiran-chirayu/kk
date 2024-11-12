pipeline {
  agent {label "ansiblecontroller"}
  stages {
    stage("checkout"){
      // Change the credentialsID appropriately
      steps {
         git branch: 'main', changelog: false, credentialsId: 'GitlabCred', poll: false, url: 'https://gitlab.com/wezvaprojects/ansible/ha-pipeline.git'
      }
    }
    stage("Execute Playbook"){
      steps {
         ansiblePlaybook installation: 'ansible2.9.6', playbook: 'sample.yml', vaultCredentialsId: 'ansiblevault'
      }
    }
  }
}
