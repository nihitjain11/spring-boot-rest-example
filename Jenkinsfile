pipeline {
    agent any
    stages{
        stage("Repo Pull"){
            steps{
                script{
                    git branch: "master", changelog: false, url: "https://github.com/nihitjain11/spring-boot-rest-example"
                }
            }
        }
        stage("maven"){
            steps{
                script{
                    withMaven (maven: "mavenTool"){
                        sh "mvn clean package"
                    }
                }
            }
        }
    }
}