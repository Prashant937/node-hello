pipeline{
    agent any
        stages('compiling stage'){
           
           steps{
             withMaven(: 'mavne_3_6_3'){
             sh 'mvn clean compile'
           }
        }
    }
       stage ('Testing Stage'){

           steps{
               withMaven(: 'mavne_3_6_3'){
             sh 'mvn test'
           }
           }
       }

       stage('Deploying Stage'){
           steps{
               withMaven(: 'mavne_3_6_3'){
             sh 'mvn deploy'
           }
           }

       }
    }
}
