pipeline {
  agent any
  stages {
    stage('GettDeployFile') {
      steps {
        httpRequest(url: 'http://localhost:30600/rest/api/submit-job/AutoDeployGetPackage', requestBody: '{"id": "last"} ', responseHandle: 'STRING', httpMode: 'POST', contentType: 'APPLICATION_JSON', acceptType: 'APPLICATION_JSON', outputFile: 'e:\\out.json')
      }
    }

  }
}