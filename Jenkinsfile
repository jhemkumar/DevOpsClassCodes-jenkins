#!/usr/bin/env groovy
import java.net.URL

node {
	stage('Git Checkout') {
		 git(
           url: 'https://github.com/jhemkumar/DevOpsClassCodes-jenkins.git',
           credentialsId: 'jhemkumar',
           branch: "master"
        )
	}
	stage('AB Compile') {
		withMaven(maven:'hemMaven') {
		    sh 'mvn compile'    
		}
		
	}
	stage('AB Package') {
		withMaven(maven:'hemMaven') {
		    sh 'mvn package'    
		}
		
	}

}