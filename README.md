# CloudFormation-Stack-with-AWS-SDK-JS-V3

<br>
<strong>
Creates/Deploys, Updates and Deletes AWS CloudFormation Stack with AWS SDK for JavaScript/NodeJS V3.
</strong>
<br><br>
The  script can execute the following:

  1) Uses the indicated YAML or JSON CloudFormation input file to create/deploy resources as specified the input file.
  
  2) Update the deployed resources.
  
  3) Delete the deployed resources.

<br>

## PURPOSE

* Normally an AWS CloudFormation stack can be deployed via AWS CloudFormation console. <br>
    
* An AWS CloudFormation stack can also be deployed via AWS-SDK in any language of choice. <br>
    
* <strong>This repository</strong> contains code for remotely deploying an AWS CloudFormation Stack via AWS SDK for JavaScript/NodeJS V3, from any computer. <br>
    
* AWS SDK for JavaScript/NodeJS V3 is very clean, light weight, very fast and it fully supports async-await syntax. <br>
    
* The sample stack used in this repo is for creating/deploying, updating and deleting an AWS Keyspace and Tables (for Apache Cassandra), used in real-time drilling, reservoir and production applications. <br><br>
    

## DEPLOYING STACK with the NodeJS script

### To deploy the stack  on ```AWS```, follow these steps:

1) #### Install NodeJS and @aws-sdk/client-cloudformation (v3) module,  assuming Ubuntu OS
   * curl -fsSL https://deb.nodesource.com/setup_19.x | sudo -E bash - <br>
   * sudo apt-get install -y nodejs <br>
   * sudo npm install @aws-sdk/client-cloudformation
    
2) #### Download or clone the following files, from this repo, into the current working directory (CWD): <br>
   * NodeJS script - index.js <br>
   * JSON files - credentials.json and inputConfig.json <br>
   

3) #### Fill in relevant values in inputConfig.json files.<br>
   * <strong>References for inputConfig.json </strong>:
     1) https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/clients/client-cloudformation/interfaces/createstackcommandinput.html
     2) https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/clients/client-cloudformation/interfaces/deletestackcommandinput.html
     3) https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/clients/client-cloudformation/interfaces/updatestackcommandinput.html

4) #### Then run the code, assuming sudo access: <br>
   * sudo node index.js


# License

Copyright © 2015 - present. MongoExpUser

Licensed under the MIT license.
