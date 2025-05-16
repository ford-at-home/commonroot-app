# Deploying Commune Connect to AWS

## Infrastructure Overview
- **Frontend**: Hosted via S3 + CloudFront
- **Backend API**: Deployed via AWS Lambda + API Gateway
- **Database**: Amazon RDS (PostgreSQL)
- **Auth**: Amazon Cognito or Supabase (external)
- **Media Uploads**: S3

## CI/CD
- GitHub Actions:
  - On push to `main`: build + deploy frontend to S3
  - Backend code deployed via Serverless Framework or CDK

## Deployment Steps

1. **Create S3 Bucket + CloudFront Distribution**  
   Upload React build to bucket  
   Set up CDN + domain via Route 53

2. **Provision RDS PostgreSQL Instance**  
   Use `terraform` or `AWS CDK` to manage credentials securely

3. **Deploy API**  
   - Use Serverless Framework or CDK to deploy Express via Lambda  
   - Add endpoint integrations via API Gateway

4. **Set Up Auth**  
   - Use Cognito User Pools or connect with Supabase Auth SDK

5. **Add Monitoring**  
   - CloudWatch for Lambda logs  
   - Sentry or LogRocket for frontend errors

---

## TODO
- Add HTTPS certs via ACM
- Set up pre-launch waitlist (e.g., Tally.so or ConvertKit)
