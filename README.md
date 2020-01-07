# Shell-ftw

#### Command to match and delete duplicate files
`find . -name '*(*).pdf' #-delete`

#### Upload a dir to s3 
```
sudo apt  install awscli
aws configure
aws s3 cp SOURCE_DIR s3://DEST_BUCKET/ --recursive
```