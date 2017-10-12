# cfn-squid-cluster

AWS CloudFormation template to create highly available Squid cluster with AWS NLB and Auto Scaling.

## Install

1. Zip squid configs in a zip archive, where `squid.conf` will be in the root directory unzipped.
2. Upload zip archive to some S3 bucket
3. Create an IAM Instance Profile and grant read access (`GetObject`) on beforementioned object to it
4. Create an CloudFormation stack and fill in parameters
5. Update ingress rules to control access to squid

## Note

1. Zipped config will be extracted to `/usr/local/squid/etc/`, with /etc/squid/squid.conf linked to /usr/local/squid/etc/squid.conf
2. It installs squid 3.4 by default, and squid should the failed doing so
