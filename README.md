Blog on aws lifecycle hook.
https://medium.com/@manojkumarcloud/auto-scaling-lifecycle-hooks-to-export-server-logs-when-instance-terminating-58e06d7c0d6a




### my FLOW

sns: instanceTerminating

policy: theASGTerminatingPolicy

role: theInstance-role

rola lambda: lambdaTheTermination-role

Lifecycle Hook:
test-hook autoscaling:EC2_INSTANCE_TERMINATING


ssm document: TerminateRunnersFirst

Lambda function: worker_instance_terminating_lambdags


******
INSTALL ssm-agent & awscli in the instances @ user-data
CHANGE configs & TAKE IMAGEs! (move all logs to the same directory  ... edit in the various .conf files)
