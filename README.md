
# aws-101
An intro to AWS delivered on Jan 20th, 2018 to NYU CUSP students, alumni and Colorado friends.
Feel free to create issues to discuss cloud topics / interview questions etc.

# Resources
- [Best **overview** of all AWS services](https://d0.awsstatic.com/whitepapers/aws-overview.pdf)
- [AWS Quick Labs](https://amazon.qwiklabs.com/catalog?locale=en)
- [History of Cloud Computing](https://www.visualistan.com/2015/09/a-brief-history-of-cloud-infographic.html)
- [EC2 Instance Comparison](https://www.ec2instances.info/)

# Getting Started with Cloud / AWS
## [Brief History of Cloud](https://www.visualistan.com/2015/09/a-brief-history-of-cloud-infographic.html)

## Mnemonics to help you grok the cloud
Think of all the things that go into firing up a jupyter notebook on your local machine.
 - Compute: Your computer's RAM
 - Storage: Your computer's HD
 - Networking: localhost and 127.0.0.1
 - Security: UserName/Password
 - Messaging: http://jupyter-client.readthedocs.io/en/stable/messaging.html
 - Application: The Browser and the Notebook itself

Now transplant this onto the cloud, specifically, AWS. All these core components exist in other cloud providers: Google's GCP and MS Azure as well. 
Refer to the overview document above for quick definitions of each of these services.

- **Compute**: EC2 instances
- **Storage**
	- Objects: S3
	- Database: RDS
- **Security**: IAM for User and Application permissions
- **Networking**: Virtual Private Cloud & Security Groups.
- **Messaging**: Application Integration service group in AWS.
- **Services**:
	- Rekognition (AWS's Image recognition API)
	- Comprehend (AWS's NLP API)
	- EMR (AWS' map-reduce, Hadoop cluster)
	- Quicksight (AWS' BI offering)
---
Docker = *Zip/RAR type program for your entire computer / application.*
EC2 configuration & launch = *Experience of buying a car. (Too many options!!)*

---


### 2 minute - 5 step Dirt simple AWS Exercise
1. Launch an EC2 instance
	2. OS = Ubuntu
	3. Instance Type = t2.micro (1GB RAM)
	4. Storage = 29 GB
	5. Networking = default settings
	6. Security Groups = Allow All Traffic or set to your home IP
	7. Key Pair = Create and download key pair. Store your **.pem** file safely and do not share it.
2. Connect to the EC2 instance
	 - `chmod 400 aws.pem`
	 - `ssh -i "aws101.pem"
   ubuntu@ec1-23-456-789-101.us-west-2.compute.amazonaws.com`
3. Create a simple HTML file (hello.html)
4. [Launch Python Simple Webserver](https://stackoverflow.com/questions/7943751/what-is-the-python-3-equivalent-of-python-m-simplehttpserver)
5. Ask your friend to connect to your instance `http://ec1-23-456-789-101.us-west-2.compute.amazonaws.com` (Works only if you allow all traffic or include your friend's IP address)

## CAUTION
- Be mindful of AWS billing.
 - Allowing all traffic on your instance opens it up to the entire internet. Understand those risks.
