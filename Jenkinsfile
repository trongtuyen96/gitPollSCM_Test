pipeline {
//   agent { label 'hiensu' }
   agent any

   stages {
      stage('Execute the test') {
         steps {
            bat """
            cd AutoTestFramework 2.2
            mvn clean test -DtestSuiteName="src/test/execution_file/${params.TEST_SUITE}"
            """
         }
      }
      
      stage('Archive report file') {
        steps {
            archiveArtifacts artifacts: 'AutoTestFramework 2.2\\reports\\*.html'
        }
      }
	}
}