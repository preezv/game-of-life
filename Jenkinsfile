node {
    stage ('scm') {
      git 'https://github.com/preezv/game-of-life.git'
  
    }
    stage ('build &package') {
        sh 'mvn package'
    }
    stage ('after test results') {
        archive 'gameoflife-web/target/gameoflife.war'
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}