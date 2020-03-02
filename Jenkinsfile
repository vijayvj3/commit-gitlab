@Library('shlib1')_
pipeline
{
    agent any
stages{
/* stage('commits')
        {
            steps{
             commits()
            // influx()
                 }
         }
        stage('contributors')
        {
            steps{
             contributors()
            // influx()
                 }
         }
     stage('issues')
        {
            steps{
             gitlab_issue()
            // influx()
                 }
         }
     stage('mergerequest')
        {
            steps{
             gitlab_mergerequest()
            // influx()
                 }
         }*/
    
    
     stage('merge_req'){
        steps{
        
            script
            {
            def ids=  Merge_request_gitlab(jsondata)
         println(ids)
          Merge_request_gitlab.commit(ids)
            }
        }
     }
/*stage('merge_req'){
        steps{
        
            script
            {
            def ids= commits_gitlabb(jsondata)
         println(ids)
     commits_gitlabb.commit(ids,jsondata)
            }
        }
     }*/

}
}
