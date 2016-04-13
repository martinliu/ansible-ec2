# stop all instances

## aws cli

`aws ec2 describe-instances --region ap-northeast-1 --filter Name=instance-state-name,Values=running --query 'Reservations[].Instances[].InstanceId' --output text | xargs aws ec2 stop-instances --region ap-northeast-1 --instance-ids
`

# start all instances

`aws ec2 start-instances --instance-ids i-5241eacd
aws ec2 start-instances --instance-ids i-794ee5e6
aws ec2 start-instances --instance-ids i-5541eaca
aws ec2 start-instances --instance-ids i-784ee5e7
aws ec2 start-instances --instance-ids i-7b4ee5e4
`

how to make this command work.
for i in $(i-5241eacd i-5541eaca i-784ee5e7 i-794ee5e6 i-7b4ee5e4); do aws ec2 start-instances --instance-ids $i; done
