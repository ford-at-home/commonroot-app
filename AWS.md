# AWS Analysis for Commune Connect

## Recommended AWS Technologies

| Component        | AWS Service            | Why It Fits                                       |
|------------------|------------------------|---------------------------------------------------|
| Frontend Hosting | S3 + CloudFront        | Scalable, fast, and cost-effective for SPA        |
| Backend          | AWS Lambda + API GW    | Serverless, scalable, and cost-efficient          |
| Database         | Amazon RDS (PostgreSQL)| Managed, reliable, supports SQL                   |
| Auth             | Amazon Cognito         | Native AWS integration, scalable auth             |
| Media Storage    | Amazon S3              | Industry standard for media and static files      |
| Monitoring       | CloudWatch             | Native monitoring and alerting                    |

## Alternatives
- Use Supabase for integrated Auth + DB (non-AWS)
- Use Firebase as a BaaS option (non-AWS)

## AWS Tutorial References
- [Host a React App on S3](https://aws.amazon.com/getting-started/hands-on/host-static-website/)
- [Deploy Node.js on Lambda](https://docs.aws.amazon.com/lambda/latest/dg/nodejs.html)
- [Set up Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html)
- [Use Cognito for Authentication](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html)
