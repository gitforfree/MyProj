pipeline {
    agent any

stage 'build'
node{
    checkout scm
    sh 'mvn clean install'
}
}
