pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn -f javademos-master/ssgsems/pom.xml -B -DskipTests clean package'
        archiveArtifacts(artifacts: '**/target/*.war', fingerprint: true)
        sh '''mkdir /home/azureuserak/buildoutput/${BUILD_NUMBER} 
cp /var/lib/jenkins/workspace/javademos_master/javademos-master/ssgsems/target/*.war /home/azureuserak/buildoutput/${BUILD_NUMBER}'''
      }
    }

  }
}