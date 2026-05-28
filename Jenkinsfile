pipeline { 
 
 agent any 
 
 stages { 
 
  stage('Clone Repository') { 
   steps { 
    git branch :'main',url :'https://github.com/Sushmithab912/exp88.git' 
   } 
  } 
 
  stage('Build Docker Image') { 
   steps { 
    bat 'docker build -t exp8 .' 
   } 
  } 
 
  stage('Run Docker Container') { 
   steps { 
    bat 'docker run -d -p 8081:80 --name web1c exp8' 
   } 
  } 
 
 } 
 
} 