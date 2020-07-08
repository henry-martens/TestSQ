node {
  stage('SCM') {
    checkout poll: false, scm: [$class: 'GitSCM', branches: [[name: 'master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/django/django.git']]]
  }
  stage('SonarQube Analysis') {
        sh "/Users/sonar-scanner-4.3.0.2102-macosx/bin/sonar-scanner -Dsonar.host.url=http://localhost:9000 -Dsonar.projectName=TestSQ -Dsonar.projectVersion=1.0 -Dsonar.projectKey=TestSQ -Dsonar.sources=. -Dsonar.projectBaseDir=/Users/a8748429/.jenkins/workspace/${JOB_NAME}"
    }
  }
