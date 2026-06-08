******************** Date: 06 Jun****************************************

--> 15 Multiple choices  
--> 1 Terraform Code 

==> #### Write S3 bucket (creation + versioning + a simple lifecycle rule) ###

provider "aws" {
  region = "us-east-1"
}

# Create S3 Bucket
resource "aws_s3_bucket" "example" {
  bucket = "my-unique-bucket-name-12345" #Creates a bucket named my-unique-bucket-name-12345
}

# Enable Versioning
resource "aws_s3_bucket_versioning" "example" {
  bucket = aws_s3_bucket.example.id  # Keeps old versions of files when they are overwritten or deleted.  

  versioning_configuration {
    status = "Enabled"
  }
}

# Lifecycle Rule
resource "aws_s3_bucket_lifecycle_configuration" "example" {
  bucket = aws_s3_bucket.example.id

  rule {
    id     = "delete-old-versions"
    status = "Enabled"

    noncurrent_version_expiration {
      noncurrent_days = 30  # Automatically removes old object versions after 30 days to save storage costs.  
    }
  }
}


terraform init
terraform apply
