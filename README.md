Blog on aws lifecycle hook.
https://medium.com/@manojkumarcloud/auto-scaling-lifecycle-hooks-to-export-server-logs-when-instance-terminating-58e06d7c0d6a




### my FLOW

policy: theASGTerminatingPolicy

role: theInstance-role

rola lambda: lambdaTheTermination-role

Lifecycle Hook:
test-hook autoscaling:EC2_INSTANCE_TERMINATING

bucket: 
{
    "Location": "/theBucket"
}


ssm document: ec2TerminationBackupLogs
 
 Lambda function: backup-ec2-logs


******
INSTALL ssm-agent & awscli in the instances @ user-data
CHANGE configs & TAKE IMAGEs! (move all logs to the same directory  ... edit in the various .conf files)


!!!!!!!!
HOW TO:
get instance-id and region from within the ec2-instance without curl (ssm document)
!!!!!!!!
