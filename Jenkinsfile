node {
  stage('SCM') {
    checkout poll: false, scm: [$class: 'GitSCM', branches: [[name: 'master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/henry-martens/TestSQ.git']]]
']]]
  }
  stage('SonarQube Analysis') {
        sh "/var/jenkins_home/tools/hudson.plugins.sonar.SonarRunnerInstallation/sonarqubescanner/bin/sonar-scanner -Dsonar.host.url=http://localhost:9000 -Dsonar.projectName=TestSQ -Dsonar.projectVersion=1.0 -Dsonar.projectKey=TestSQ -Dsonar.sources=. -Dsonar.projectBaseDir=/var/jenkins_home/workspace/${JOB_NAME}"
    }
  }
