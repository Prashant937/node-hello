pipeline{
    agent any
        stages('compiling stage'){
           
           steps{
             withMaven(maven : 'mavne_3_6_3'){
             sh 'mvn clean compile'
           }
        }
    }
       stage ('Testing Stage'){

           steps{
               withMaven(maven : 'mavne_3_6_3'){
             sh 'mvn test'
           }
           }
       }

       stage('Deploying Stage'){
           steps{
               withMaven(maven : 'mavne_3_6_3'){
             sh 'mvn deploy'
           }
           }

       }
    }
}
