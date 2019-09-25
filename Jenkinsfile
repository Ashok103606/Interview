node {
    stage('SCM Checkout'){
    git 'https://github.com/Ashok103606/Interview.git'
    }
    stage('Compile-Package'){
     def mvnHome = tool name: 'maven-3', type: 'maven'
     sh "${M2_Home}/bin/mvn package"
     }
    stage('Email'){
    mail bcc: '', body: 'Hi, this is Ashok . details about your recent commit build.',
    cc: '', from: '', replyTo: '', subject: 'Project Build information',
    to: 'ashokddevops@gmail.com'
    }
}
