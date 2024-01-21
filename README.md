# pullrequest-jenkins

we are just testging pull request trigger jenkins pipeline 

Creating job:
Create a new job.

Add the project's GitHub URL to the "GitHub project" field (the one you can enter into browser. eg: "https://github.com/janinko/ghprb")

Select Git SCM.

Add your GitHub "Repository URL".

Under Advanced, set "refspec" to

+refs/pull/*:refs/remotes/origin/pr/*
In "Branch Specifier", enter

${sha1}
or if you want to use the actual commit in the pull request, use

${ghprbActualCommit}

--------------------------------------------
Go to jenkins create a new jenkins freestyle job github account url above
<img width="676" alt="image" src="https://github.com/harsha-209/pullrequest-jenkins/assets/51083187/d5505edd-963b-4754-adc5-6df73bbf04d0">

follow second step in source code use code clone url
<img width="676" alt="image" src="https://github.com/harsha-209/pullrequest-jenkins/assets/51083187/5e0c45f5-be21-4179-82d7-e7026a463a7c">

<img width="669" alt="image" src="https://github.com/harsha-209/pullrequest-jenkins/assets/51083187/4f5fc905-9cfc-4ed0-8c3d-ce24485df58c">
select github pull request section like below screenshot
<img width="916" alt="image" src="https://github.com/harsha-209/pullrequest-jenkins/assets/51083187/902c029b-516c-46c5-8519-a32a64d5206d">

click on below setting like fill 
<img width="665" alt="image" src="https://github.com/harsha-209/pullrequest-jenkins/assets/51083187/b7d2f888-9a46-48b5-be37-bb079cd81bdb">

click on trigger setup add below like this 
<img width="628" alt="image" src="https://github.com/harsha-209/pullrequest-jenkins/assets/51083187/ae00509a-27bd-43f4-a19c-6e3d19bf6df3">
<img width="641" alt="image" src="https://github.com/harsha-209/pullrequest-jenkins/assets/51083187/2c22a6b5-3515-44cb-bce4-ee1c21997ebb">


