# Test 01

So this is the first test of github integration with the docs-site app running on k8s.

I'll merge this branch and it should call the AWS lambda exposed through AWS API Gateway.

The Lambda function will pull the docs repository stored on the NFS server and then trigger a rollout of the docs-site
deployment on the k8s cluster. Well, let's see.

## Update 01

Ok, first problem is here: the lambda function should care only about push events with reference to the `MASTER` head,
so when you push a commit to a branch, the lambda should ignore it.

I have made the change and deployed new version, so let's see with this commit now.


## Update 02

So far so good. Another test - direct push to the master, without a pull request, should work too, let's see...


## Update 03

So far it works pretty good. It does have also Slack notifications, more spam, yay!

Now it's time to unfuck the code a bit and finally introduce CI for the application itself, hurray, only few month
delay, awesome!!!
