docker-ebs-attach
==============

Docker container that attaches an EBS volume to the local ec2 instance. The volume is identified by its Name tag.

Usage:

```
docker run -it --rm leg100/ebs-attach \
--volume-name MyVolumeName \
--device /dev/xvdf \
--region eu-west-1
```

Note: it relies on the ec2 instance possessing an IAM profile with the following privileges:

 - ec2:AttachVolume
 - ec2:DetachVolume
