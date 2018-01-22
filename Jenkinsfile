pipeline {
  agent {
    label "jenkins-maven"
  }
  stages {
    stage('Maven Release') {
      steps {
        mavenFlow {
          cdOrganisation "jstrachan"
          useStaging false
          useSonatype false
          pauseOnFailure true

          promoteArtifacts {
            pre {
              echo "====> hook invoked before promote artifacts!"
            }
          }
        }
      }
    }
  }
}
