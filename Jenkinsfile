pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    
    environment {
        SNAP_REPO = 'kavya123-snapshot'
		NEXUS_USER = 'admin'
		NEXUS_PASS = 'Admin1234'
		RELEASE_REPO = 'kavya123-release'
		CENTRAL_REPO = 'kavya123-maven-dependencies'
		NEXUSIP = '172.31.89.241'
		NEXUSPORT = '8081'
		NEXUS_GRP_REPO = 'kavya123-maven-grp'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}