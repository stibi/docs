# Test 01

So this is the first test of github integration with the docs-site app running on k8s.

I'll merge this branch and it should call the AWS lambda exposed through AWS API Gateway.

The Lambda function will pull the docs repository stored on the NFS server and then trigger a rollout of the docs-site
deployment on the k8s cluster. Well, let's see.
