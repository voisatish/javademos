pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn -f javademos/javademos-master/pom.xml -B -DskipTests clean package'
      }
    }

  }
}