# Overview

- AWS CLI allows a machine to get access to various operations to control AWS resources. 
- It is typically installed via [Choco](choco.md) on Windows
- After installing AWS CLI, run the following command to establish access based on access key and default region
  ```
  aws configure
  
  sample output:
  AWS Access Key ID [****************abcd]:
  AWS Secret Access Key [****************wxyz]:
  Default region name [us-east-1]:
  Default output format [json]:
  
  aws --version
  
  sample output:
  aws-cli/2.27.21 Python/3.13.3 Windows/11 exe/AMD64
  ```

Back to [index](index.md)