# How to get AWS Metadata
run the following command with super user(sudo)
curl http://169.254.169.254/latest/meta-data/
after executing the command you will see the following output -->
(ami-id, ami-launch-index ,ami-manifest-path, block-device-mapping/ , events/, hibernation/ , hostname , identity-credentials/ , instance-action , instance-id ..etc)
Now u can check the details of metadata by using the below command
curl http://169.254.169.254/latest/meta-data/events/     -->to check AMI ID of your ec2
curl http://169.254.169.254/latest/meta-data/ami-id      --> to find events

**#How to get AWS Dynamic data**
curl http://169.254.169.254/latest/dynamic/
output -->  instance-identity/
curl http://169.254.169.254/latest/dynamic/instance-identity/
output -->
rsa2048
document
pkcs7
signature
curl http://169.254.169.254/latest/dynamic/instance-identity/document/
output -->
  {
  "accountId" : "725799283397",
  "architecture" : "x86_64",
  "availabilityZone" : "ap-south-1a",
  "billingProducts" : null,
  "devpayProductCodes" : null,
  "marketplaceProductCodes" : null,
  "imageId" : "ami-0d758c1134823146a",
  "instanceId" : "i-035b3fdd5338aca77",
  "instanceType" : "t2.micro",
  "kernelId" : null,
  "pendingTime" : "2021-03-31T05:44:30Z",
  "privateIp" : "10.0.0.167",
  "ramdiskId" : null,
  "region" : "ap-south-1",
  "version" : "2017-09-30"
}
