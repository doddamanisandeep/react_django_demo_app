pipeline{
    agent any
    stages{
        stage("CLone the code"){
            steps{
                git url: 'https://github.com/doddamanisandeep/react_django_demo_app.git', branch:'main'
                echo "code cloned"
            }
        }
        
        stage("Build") {
            steps{
                
               sh  "docker build -t react_django_demo_app ."
               echo "image built..."
            }
        }
        
        stage("Create container") {
            steps{
            sh "docker run -d -p 8001:8001 react_django_demo_app"
            echo "container created"
            }
        }
        
        
    }
    
    
}
