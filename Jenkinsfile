pipeline
{
   agent any
   stages
   {
      stage('execute cucumber tests')
      {
          steps
          {
             bat "docker-compose up"
          }
      }
      
      stage('Bring docker compose down')
      {
          steps
          {
             bat "docker-compose down"
          }
      }
   }

}