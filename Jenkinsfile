node{

    stage('SCM Checkout')
    {
        //git url: 'https://github.com/deomca/online-shop.git'
     git credentialsId: '1e40ecf7-77df-41c6-a8d4-dd15eee36d72', url: 'https://github.com/VardhanNS/phpmysql-app.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u upasanatestdocker -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "deomca" -p "osho3827" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push deomca/job1_web2.0'
            // sh 'docker push upasanatestdocker/mysql'
          
    } 
}
