# secure-bucket

Creates a S3 bucket with access logging enabled.

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| terraform | >= 0.12 |
| aws | >= 3.0.0 |

## Providers

| Name | Version |
|------|---------|
| aws | >= 3.0.0 |

## Modules

No Modules.

## Resources

| Name |
|------|
| [aws_iam_policy_document](https://registry.terraform.io/providers/hashicorp/aws/3.0.0/docs/data-sources/iam_policy_document) |
| [aws_s3_bucket](https://registry.terraform.io/providers/hashicorp/aws/3.0.0/docs/resources/s3_bucket) |
| [aws_s3_bucket_policy](https://registry.terraform.io/providers/hashicorp/aws/3.0.0/docs/resources/s3_bucket_policy) |
| [aws_s3_bucket_public_access_block](https://registry.terraform.io/providers/hashicorp/aws/3.0.0/docs/resources/s3_bucket_public_access_block) |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| bucket\_name | n/a | `any` | n/a | yes |
| enabled | A boolean that indicates this module is enabled. Resources are not created if it is set to false. | `bool` | `true` | no |
| force\_destroy | A boolean that indicates all objects should be deleted from the bucket so that the bucket can be destroyed without error. These objects are not recoverable. | `bool` | `false` | no |
| lifecycle\_glacier\_transition\_days | The number of days after object creation when the object is archived into Glacier. | `number` | `90` | no |
| log\_bucket\_name | n/a | `any` | n/a | yes |
| tags | Specifies object tags key and value. This applies to all resources created by this module. | `map` | <pre>{<br>  "Terraform": true<br>}</pre> | no |

## Outputs

| Name | Description |
|------|-------------|
| log\_bucket | The S3 bucket used for storing access logs of this bucket. |
| this\_bucket | This S3 bucket. |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
