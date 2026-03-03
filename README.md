# Terraform AWS Static Portfolio

Projet 1 : provisionnement IaC d'un site statique sur AWS S3 avec Terraform.

## Stack
- Terraform
- AWS S3 Static Website Hosting
- AWS CLI (profil `terraform`)

## Ressources créées
- `aws_s3_bucket`
- `aws_s3_bucket_website_configuration`
- `aws_s3_bucket_public_access_block`
- `aws_s3_bucket_policy`
- `random_string`

## Déploiement
```bash
export AWS_PROFILE=terraform
terraform init
terraform validate
terraform plan
terraform apply -auto-approve
```

## Upload du site
```bash
aws s3 sync site/ s3://<bucket_name>
```

## Endpoint
- Bucket: `yacine-portfolio-1sziirdx`
- Website: http://yacine-portfolio-1sziirdx.s3-website-eu-west-1.amazonaws.com
