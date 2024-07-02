# Terraform S3 Bucket and Website Configuration

This repository contains Terraform code for creating an AWS S3 bucket, configuring it for website hosting, and uploading static files (HTML and images) to it. The configuration also includes setting up necessary bucket policies and access controls.

## Project Structure
```bash
├── main.tf
├── provider.tf
├── variables.tf
├── output.tf
├── website
│   ├── index.html
│   ├── error.html
│   └── images
│       └── profile.jpg
└── README.md
```
## Prerequisites

- [Terraform](https://www.terraform.io/downloads.html) (v0.14+)
- AWS account with necessary permissions to create S3 buckets and manage S3 resources.
- AWS CLI configured with appropriate credentials.

## Setup Instructions

1. **Clone the repository**
    ```sh
    git clone https://github.com/yourusername/terraform-s3-website.git
    cd terraform-s3-website
    ```

2. **Initialize Terraform**
    ```sh
    terraform init
    ```

3. **Set the required variables**
    Create a `terraform.tfvars` file or set environment variables with the necessary values:
    ```plaintext
    bucketname = "your-unique-bucket-name"
    ```

4. **Run Terraform Plan**
    ```sh
    terraform plan
    ```

5. **Apply the Terraform configuration**
    ```sh
    terraform apply
    ```


## Testing the Website

Once the Terraform configuration is applied successfully, you can access the website using the S3 bucket URL. You can find the website URL in the Terraform output after applying the configuration.

## Cleanup

To remove the resources created by Terraform, run:
```sh
terraform destroy
```

Enter `yes` when prompted to confirm the deletion of resources.



## Troubleshooting

- Ensure your AWS credentials are correctly configured.
- Check the AWS S3 console to verify the bucket and objects are created.
- Review the Terraform logs for any error messages and refer to the [Terraform documentation](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket_website_configuration) for further guidance.

