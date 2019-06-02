
        stage ('Scm Checkout'){
node{
        stage ('Scm Checkout'){
            git credentialsId: 'github', url: 'https://github.com/soniyakarade/spring-framework-petclinic.git'}
        
        stage('build')
            sh 'mvn clean install'
        
        stage ('Step 1st'){
            sh '/usr/bin/docker build -t soniyakarade/test-2:v2 .'}
    
        stage ('push docker image'){
            withCredentials([usernamePassword(credentialsId: 'devops-practice', passwordVariable: 'pushpwd', usernameVariable: 'pushimage')]) 
            {
                sh '/usr/bin/docker login -u $pushimage -p $pushpwd'
            }
        
                sh '/usr/bin/docker push soniyakarade/test-2:v2'
        
        }
    }it credentialsId: 'github', url: 'https://github.com/soniyakarade/centos7docker.git'}

    stage ('Scm build'){
    sh '/usr/bin/docker build -t soniyakarade/test-1:v1 .'}
    
    stage ('push docker image'){
        withCredentials([usernamePassword(credentialsId: 'devops-practice', passwordVariable: 'pushpwd', usernameVariable: 'pushimage')]) 
        {
            sh '/usr/bin/docker login -u $pushimage -p $pushpwd'
        }
        
            sh '/usr/bin/docker push soniyakarade/test-1:v1'
        
        
    }

D
}
