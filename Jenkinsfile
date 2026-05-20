pipeline{
  agent any
  stages{
    stage('Test'){
      steps{
        script{  
          echo 'Testing Process'      
        }
      }
    }  

    stage('Build'){
      steps{
        when{
          expression{
            BRANCH_NAME == 'master'
          }
        }
        script{   
          echo 'Building Process'     
        }
      }
    }

    stage('Deploy'){
      steps{
        when{
          expression{
            BRANCH_NAME == 'master'
          }
        }
        script{    
          echo 'Deploying Process'    
        }
      }
    }  
  }
}
