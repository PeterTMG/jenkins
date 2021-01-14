pipeline {
  agent any
  stages {
    stage('GettDeployFile') {
      steps {
        httpRequest(url: 'https://localhost:30600/rest/api/submit-job/AutoDeployGetPackage', requestBody: '{"id": "last"} ', responseHandle: 'STRING', httpMode: 'POST', contentType: 'APPLICATION_JSON', acceptType: 'APPLICATION_JSON', outputFile: 'e:\\out.json', ignoreSslErrors: true)
      }
    }

    stage('SendDeployToTest') {
      steps {
        httpRequest(url: 'https://localhost:30600/rest/api/submit-job/AutoDeployTest', acceptType: 'APPLICATION_JSON', contentType: 'APPLICATION_JSON', httpMode: 'POST', uploadFile: 'e:\\out.json', responseHandle: 'STRING', ignoreSslErrors: true)
      }
    }

  }
}