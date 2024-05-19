pipeline
{
   agent any
   stages
   {

      stage('Pull the image')
      {
          steps
          {
             bat "docker pull attbatch1/entireconfigurationinyaml"
          }
      }

      stage('Start the Grid')
      {
          steps
          {
             bat "docker-compose up -d hub chrome firefox"
          }
      }

      stage('executing cucumber testcases')
      {
          steps
          {
             bat "docker-compose up cucumbertestcases"
          }
      }
   }

   post{

      always
      {

         bat "docker-compose down"
      }


   }

}