node('mavenlarge-gol') {
    
    stage('SCM') { 
    sh label: '', script: 'https://github.com/shopizer-ecommerce/shopizer.git'
}
   stage('ecommerce-build') {
    sh label: '', script: '''cd ecommerce-pipeline
mvn clean package -DskipTests'''
}
stage('archivewar') {
    archiveArtifacts artifacts: 'sm-shop/target/ROOT.war', followSymlinks: false
}

}
