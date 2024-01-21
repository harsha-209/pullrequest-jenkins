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


part2
Creating a job:
Create a new job.
Add the project's GitHub URL to the GitHub project field (the one you can enter into browser. eg: https://github.com/janinko/ghprb)
Select Git SCM.
Add your GitHub Repository URL.
Under Advanced, set Name to origin and:
If you just want to build PRs, set refspec to +refs/pull/${ghprbPullId}/*:refs/remotes/origin/pr/${ghprbPullId}/*
If you want to build PRs and branches, set refspec to +refs/heads/*:refs/remotes/origin/* +refs/pull/${ghprbPullId}/*:refs/remotes/origin/pr/${ghprbPullId}/* (see note below about parameterized builds)
In Branch Specifier, instead of the default */master, enter
${ghprbActualCommit} if you want to use the head of the pull request branch (e.g. refs/pull/4/head); or
${sha1}, to use GitHub's tentative merge of the compare and base branches (e.g. refs/pull/4/merge) if the PR can be automatically merged or the head of the pull request branch (e.g. refs/pull/4/head) if they can not be automatically merged.
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


Now go to manage jenkins and select configure and search for github pull request builder please provide personal access token here as  a secrete and click on test api connection
<img width="881" alt="image" src="https://github.com/harsha-209/pullrequest-jenkins/assets/51083187/2882a484-1ac3-4879-abd6-3cff5acabde4">

git hub webhook setup and provide personal access token here
<img width="557" alt="image" src="https://github.com/harsha-209/pullrequest-jenkins/assets/51083187/7952e262-3911-4d36-8fae-04a158fd77e9">


https://plugins.jenkins.io/ghprb/

https://github.com/jenkinsci/ghprb-plugin

exit
