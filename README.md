# Static Website Hosting on Amazon S3

A personal portfolio website hosted on **Amazon S3** using static website hosting. I built this hands-on project while preparing for the **AWS Certified Cloud Practitioner** exam, to practise core S3 and access-control concepts.

## AWS services and concepts used

- **Amazon S3**: bucket and objects
- **Static website hosting**: index document and error document
- **Bucket policy**: JSON policy allowing public read access
- **Block Public Access**: turned off for this bucket only, because it holds public website files
- **Region**: Asia Pacific (Hyderabad) `ap-south-2`

## Project files

| File | Purpose |
|------|---------|
| `index.html` | Home page of the website |
| `error.html` | Custom error page shown for wrong URLs |
| `style.css` | Styling for the pages |
| `bucket-policy.json` | Bucket policy template (not uploaded to the bucket) |

> **Note:** The starter website files were generated with the help of an AI assistant. I customised the content, tested the pages, and did the AWS setup myself.

## Steps I followed

1. Created an S3 bucket in `ap-south-2` with a globally unique name.
2. Turned off Block Public Access for the bucket.
3. Uploaded `index.html`, `error.html` and `style.css`.
4. Added the bucket policy from `bucket-policy.json`.
5. Enabled static website hosting with `index.html` and `error.html`.
6. Tested the website using the bucket website endpoint.

## What I learned

- The difference between a bucket and an object
- Why objects are private by default and how bucket policies grant access
- How static website hosting works, and that S3 website endpoints only support HTTP
- The shared responsibility model: AWS secures the infrastructure, I manage access to my data
- Why public buckets are a security risk

## Security notes

- This bucket contains only public website files.
- No access keys, passwords or personal data are stored in this repository.

## Future improvements

- [ ] Add Amazon CloudFront for HTTPS and faster delivery
- [ ] Use Amazon Route 53 for a custom domain
- [ ] Recreate the setup using Terraform
- [ ] Automate deployment with GitHub Actions

## Author

**Tamil Selvi**, BSc Computer Science student, Chennai, India
GitHub: [tamil-selvi05](https://github.com/tamil-selvi05)
