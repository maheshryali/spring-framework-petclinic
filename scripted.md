pipeline script :

    node('SPRING') {
         stage('spring1') {
         git url:'https://github.com/maheshryali/spring-framework-petclinic.git',
          branch: 'master'
}
 stage('bulid'){
   sh 'mvn package'  
 }
}