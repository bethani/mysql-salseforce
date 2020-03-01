pipeline {
    agent any 
    stages {
        stage('Build Application') { 
            steps {
                
                bat "mvn clean install"
            }
        }
        stage('Test Application') { 
            steps {
              bat "mvn clean test" 
            }
        }
        stage('Deploy Application') { 
            steps {
             bat "mvn clean package deploy -Dmule.version=4.2.2 -Dusername=tigest -Dpassword=Ethiopia1@ -Dworkers=1 -Dworker.type=Micro -Denvironment=Sandbox -Dapplication.name=salesforceMysqle -DmuleDeploy"
            }
        }
    }
}