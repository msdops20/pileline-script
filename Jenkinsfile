node('mavenlarge-gol') {
    stage('rmdir'){ 
    sh label: '', script: '''rm -fv *.*
rm -rf *'''
}
    stage('SCM') { 
    sh label: '', script: 'https://github.com/shopizer-ecommerce/shopizer.git'
}
   stage('ecommerce-build') {
    sh label: '', script: 'mvn clean package -DskipTests'
}
stage('archivewar') {
    archiveArtifacts artifacts: 'sm-shop/target/ROOT.war', followSymlinks: false
}

}
