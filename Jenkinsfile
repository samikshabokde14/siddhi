pipeline{
         agent any
       stages{
           stage( checkout ){
             steps{
                 git 'https://github.com/samikshabokde14/siddhi.git'
                }
             }
           stage( build ){
              steps{
                   sh 'mvn install'
                 }
                }
           stage( deployment ){
              steps{
                   sh 'cp target/siddhi.war /home/samiksha/Downloads/apache-tomcat-9.0.93/webapps'
                 }
               }
             }
          }


