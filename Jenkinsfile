#!usr/bin/env groovy
@Library('jenkins-shared-library')
def gv
pipeline{
  agent any
  tools{
    maven 'maven_3.9'
  }
  stages{
    stage('init'){
      steps{
        script{
          gv = load "script.groovy"
        }
      }
    }

    stage('BuildJar'){
      steps{
        script{
          buildJar()
        }
      }
    }

    stage('BuildImage'){
      steps{
        script{
          buildImage()
        }
      }
    }

    stage('Deploy'){
      steps{
        script{
          gv.Deploy()
        }
      }
    }
    
  }
}