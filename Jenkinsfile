node('mavenlarge-gol') {
    
    stage('SCM') { 
    git 'https://github.com/shopizer-ecommerce/shopizer.git'
}
   stage('ecommerce-build') {
    sh label: '', script: 'mvn clean package -DskipTests'
}
stage('archivewar') {
    archiveArtifacts artifacts: 'sm-shop/target/ROOT.war', followSymlinks: false
}

}
