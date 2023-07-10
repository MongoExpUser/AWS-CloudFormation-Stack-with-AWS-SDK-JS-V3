[![CI - AWS-SDK-JS-V3 Deploy CFN](https://github.com/MongoExpUser/AWS-CloudFormation-Stack-with-AWS-SDK-JS-V3/actions/workflows/deploy-cfn.yml/badge.svg)](https://github.com/MongoExpUser/AWS-CloudFormation-Stack-with-AWS-SDK-JS-V3/actions/workflows/deploy-cfn.yml)

# CloudFormation-Stack-with-AWS-SDK-JS-V3

<br>
<strong>
Creates/Deploys, Updates and Deletes AWS CloudFormation Stack with AWS SDK for JavaScript/NodeJS V3.
</strong>
<br><br>
The  script can execute the followings:

  1) Uses the indicated YAML or JSON CloudFormation input file to create/deploy resources as specified in the input file.
  
  2) Updates the deployed resources.
  
  3) Deletes the deployed resources.

<br>

## PURPOSE

* Normally an AWS CloudFormation stack can be deployed via AWS CloudFormation console or AWS CLI. <br>
    
* An AWS CloudFormation stack can also be deployed via AWS SDK in any language of choice. <br>
    
* <strong>This repository</strong> contains code for deploying an AWS CloudFormation stack via AWS SDK for JavaScript/NodeJS V3, from any computer. <br>
    
* AWS SDK for JavaScript/NodeJS V3 is clean, light weight, fast and it fully supports async-await syntax. <br>
    
* The sample stack (<strong>keyspace.yaml</strong> file) in this repository is for creating/deploying, updating and deleting an AWS Keyspace and Tables (for Apache Cassandra), used in real-time drilling, reservoir and production applications. <br><br>
    
    
## DEPLOYING STACK with the NodeJS script

## OPTION 1: Clone to Local Computer

### To deploy the stack  on ```AWS```, follow these steps:

1) #### Install NodeJS and @aws-sdk/client-cloudformation (v3) module,  assuming Ubuntu OS
   * curl -fsSL https://deb.nodesource.com/setup_19.x | sudo -E bash - <br>
   * sudo apt-get install -y nodejs <br>
   * sudo npm install @aws-sdk/client-cloudformation
    
2) #### Download or clone the following files, from this repo, into the current working directory (CWD): <br>
   * NodeJS script:  index.js <br>
   * JSON files: credentials.json and inputConfig.json <br>
   * CloudFormation YAML input file:  keyspace.yaml <br>
   

3) #### Fill in relevant values in inputConfig.json file.<br>
   * <strong>References for inputConfig.json </strong>:
     1) https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/clients/client-cloudformation/interfaces/createstackcommandinput.html
     2) https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/clients/client-cloudformation/interfaces/deletestackcommandinput.html
     3) https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/clients/client-cloudformation/interfaces/updatestackcommandinput.html

4) #### Then run the code, assuming sudo access: <br>
   * sudo node index.js <br><br>
   
   
   
## OPTION 2: Through GitHub Actions

### This option has the benefits of CICD in general. To deploy the stack  on ```AWS```, via GitHub action, follow these steps:

1)  #### Check and fill relevant values in the GitHub Actions YML deployment file.
    * Link: https://github.com/MongoExpUser/AWS-CloudFormation-Stack-with-AWS-SDK-JS-V3/blob/main/.github/workflows/deploy-cfn.yml
  
2)  #### Also fill relevant values in the inputConfig.json file.
    * Ensure that the environment (dev, stag or prod) and region in the file correspond to the values in the GitHub Actions YML file. <br>
  
3)  #### Add the actual values for credentials to the GitHub Secrets.
    * These include: <strong> accessKeyId, secretAccessKey and region.</strong>
    * This prevents exposure of the credentials.

4)  #### Then enable GitHub Actions Workflow and run the YML file.
    * Link: https://github.com/MongoExpUser/AWS-CloudFormation-Stack-with-AWS-SDK-JS-V3/actions <br><b>
  


# License

Copyright © 2015 - present. MongoExpUser

Licensed under the MIT license.
