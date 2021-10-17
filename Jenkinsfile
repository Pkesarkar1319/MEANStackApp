node {
  stage('SCM') {
    checkout poll: false, scm: [$class: 'GitSCM', branches: [[name: 'refs/heads/develop']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/Pkesarkar1319/MEANStackApp/edit/develop/Jenkinsfile']]]
  }
  stage('SonarQube Analysis') {
        sh "/home/jenkins/tools/hudson.plugins.sonar.SonarRunnerInstallation/sonarqubescanner/bin/sonar-scanner -Dsonar.host.url=http://192.162.19.1:9000 -Dsonar.projectName=sonar_jenkins1 -Dsonar.projectVersion=9.1  -Dsonar.sources=. -Dsonar.projectBaseDir=/home/jenkins/workspace/sonar_jenkins_pipeline"
    }
  }
