node {
    // This displays colors using the 'xterm' ansi color map.
    ansiColor('xterm') {
        // Just some echoes to show the ANSI color.
        stage('checkout') {
          checkout scm
        }
        stage('build') {
          sh 'zip pythonscript.zip app.py util.py'
        }
        stage('deploy') {
          sh 'aws s3 cp pythonscript.zip s3://fresh-project/'
        }
    }
}
