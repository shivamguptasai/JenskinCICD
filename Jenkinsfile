pipeline{
    agent any
    
    environment {
        dotnet ='C:\\Program Files (x86)\\dotnet\\'
        }
        stages { stage('Checkout') {
    steps {
   checkout scm
   }
   }
   stage('Build'){
   steps{
   bat "dotnet restore"" 
      bat "dotnet build --configuration Release"
    }
 }
 stage('Publish'){
     steps{
       bat "dotnet publish --no-restore --configuration Release --output .\\publish"
     }
}
post{
  success{
    echo 'Build Test And publish Successfully'
    }
  }
 }
 }