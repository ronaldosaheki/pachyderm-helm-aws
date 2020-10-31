Contributing
===

How to create a new version 
---


You will need the pachyderm cli tool for the current version supported by this repo:
eg: 1.10.5

And also download the latest pachyderm cli to which you want to upgrade this repo:
eg: 1.11.5

Download from:

Run the following command in both version:
```
pachctl_1.10.5 deploy amazon ${BUCKET_NAME} ${AWS_REGION} ${STORAGE_SIZE} --dynamic-etcd-nodes=1 --iam-role ${IAM_ROLE} --dry-run
pachctl_1.11.5 deploy amazon ${BUCKET_NAME} ${AWS_REGION} ${STORAGE_SIZE} --dynamic-etcd-nodes=1 --iam-role ${IAM_ROLE} --dry-run
```

And diff the output and implement the different in the Helmchart template.

Update helm charts
---
```
helm package .
helm repo index .
```
