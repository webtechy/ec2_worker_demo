Referenced the following guide:
https://spacelift.io/blog/spacelift-worker-pool-on-ec2

1) openssl req -new -newkey rsa:4096 -nodes -keyout spacelift.key -out spacelift.csr

2) Manual creation of Spacelift API key goto "Create API key" https://webtechy.app.spacelift.io/settings/api-keys

3) Saved generated "api-key-worker_pool.config" file which will be used for "TF_VAR_spacelift_api_key_secret"

4) AWS Cloud Integration: https://docs.spacelift.io/integrations/cloud-providers/aws

5) Generate Spacelift’s mothership IPS
6) Network setup, 2 subnets and 2 sgs
Ingress: 443 for all Spacelift Mothership IPs
Egress: 443 for 0.0.0.0/0

7) Generate Worker Pool:
https://spacelift.io/blog/spacelift-worker-pool-on-ec2#generating-the-worker-pool

8) Fork/Create repo for worker module
https://spacelift.io/blog/spacelift-worker-pool-on-ec2#create-a-repository-that-uses-the-worker-pool-module

9) Create Stack
https://spacelift.io/blog/spacelift-worker-pool-on-ec2#create-the-worker-pool-stack

9a) Stack env params
Entered the following Stack params in spacelift Stack: 
https://webtechy.app.spacelift.io/stack/aru-awesome-worker/environment

TF_VAR_spacelift_api_key_endpoint
https://webtechy.app.spacelift.io/

TF_VAR_spacelift_api_key_id
01HV4JM7ER2Q61ZMY8XYDZP76N

TF_VAR_spacelift_api_key_secret
#*****


TF_VAR_worker_pool_config
#*****

TF_VAR_worker_pool_id
01HV4WZ2TC3CGG33GSW3SR182T

TF_VAR_worker_pool_private_key
cat spacelift.key |base64 -b 0 |pbcopy

TF_VAR_worker_pool_security_groups
["sg-043d33156c94f0076", "sg-0f6529e3768a68069"]

TF_VAR_worker_pool_subnets
["subnet-036d327d023f9797f", "subnet-07b01a0301b3cbb01"]


10) Run/trigger Stack

11) Fix any IAM perm issues for IAM role:
https://docs.spacelift.io/integrations/cloud-providers/aws#setup-a-role-in-aws
(i.e., EC2, Cloudwatch, Lambda, SSM, Eventbridge, etc.) can be better optimized with more specific IAM policy

12) Check CloudWatch Logs for any issues:
https://us-west-2.console.aws.amazon.com/cloudwatch/home?region=us-west-2#logsV2:live-tail$3FlogGroupArns$3D~(~'arn*3aaws*3alogs*3aus-west-2*3a471112774192*3alog-group*3a*2faws*2flambda*2fsp5ft-01HV4WZ2TC3CGG33GSW3SR182T-ec2-autoscaler*3a*2a)

13) Re-run Spacelift stack if needed to re-apply any unapplied/unconfirmed changes:
https://webtechy.app.spacelift.io/stack/aru-awesome-worker/run/01HV4YD92AN3E683P579M242MM
