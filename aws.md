# AWS

## List all files
```
aws s3 ls s3://bucket-name/
```

## Copy all files
```
aws s3 cp s3://bucket-name/ . --recursive
```

## Copy one file
```
aws s3 cp s3://bucket-name/{filename} .
```
