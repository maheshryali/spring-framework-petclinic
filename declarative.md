pipeline script :

    node('SPRING') {
 pipeline{   
    agent {label 'SPRING'}
     stages {
         stage('spring1') {
         steps{
         git url:'https://github.com/maheshryali/spring-framework-petclinic.git',
          branch: 'master'
}
        }
        }
 stage('bulid'){
 steps{
   sh 'mvn package'  
 }
}
    }
    }
}
}