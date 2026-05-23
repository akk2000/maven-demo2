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
      when{
          expression{
            BRANCH_NAME == 'main'
          }
        }
      steps{
        script{   
          echo 'Building Process'     
        }
      }
    }

    stage('Deploy'){
      when{
          expression{
            BRANCH_NAME == 'main'
          }
        }
      steps{
        script{    
          echo 'Deploying Process'    
        }
      }
    }  
  }
}
