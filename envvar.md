Referenced the following guide:
https://spacelift.io/blog/spacelift-worker-pool-on-ec2


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
