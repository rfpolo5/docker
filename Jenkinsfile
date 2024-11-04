pipeline{
    agent {
      dockerfile{
        filename "Dockerfile"
        dir "."
        additionalBuildArgs "--tag rafaelpolo/temperaturas"
        args "-p 9191:80"
      }
    } 

    stages{

      stage("build app"){
        steps{
          echo "build...."
        }
      }
      stage("execute app"){
        steps{
          sh "python /app/temperature.py"
        }
      }
    }
}
