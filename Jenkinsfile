#!/usr/bin/env groovy
import java.net.URL
node{
    stage('git checkout'){
        git 'https://github.com/GaneshBabu2021/DevOpsClassCodes.git'
    }
    stage('AB Compile'){
        withMaven(maven:'my maven'){
            sh 'mvn compile'
        }
    }
    stage('AB Review'){
        withMaven(maven:'my maven'){
            sh 'mvn pmd:pmd'
        }
    }
    stage('AB Package'){
        withMaven(maven:'my maven'){
            sh 'mvn package'
        }
    }
}
