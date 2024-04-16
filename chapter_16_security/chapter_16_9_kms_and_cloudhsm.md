# Chapter 16.9 Managing Encryption Keys with Key Management Service (KMS) and CloudHSM

What is AWS KMS?
- key management service
- makes it easy to create and control encryption keys used to encrypt data
- managing encryption keys
- integrates with other services
- centralized control of keys, who can manage and use them

Encryption Keys
- CMK : customer master key - the logical representation of a master key
- contains key material to encrypt and decrypt data
- request creation

- HSM : physical computing device that safeguards and manages digital keys and performs encryption and decryption function

Generate a CMK
- AWS creates the CMK for you
- import key material from your own key management infra
- have the key material generated and used in a CloudHSM cluster

Key Rotations
- can choose the have KMS rotate CMKs every year if you had AWS generate the CMK for you using their own HSM
- not supported for keys generated in CloudHSM of customer services outside AWS

Policies
- manage access to your CMKs based on policies
- KMS CMKs have key policies
- can use key policy, use grants, IAM policies

What is AWS CloudHSM?
- cloud based HSM that enables you to use your own encryption keys on the AWS cloud
- physical device dedicated to you
- highly available

KMS vs. CloudHSM
- KMS is shared tenancy of underlying hardware
	- automatic key rotation and generation
- CloudHSM is dedicated to you and you have full control over underlying hardware
	- no automatic key rotation

Exam Tips
- KMS makes it easy to create and control encryption keys
- start by requesting a CMK
	- you control lifecycle of CMK and who can use it
- generate CMK by 1) AWS creates it for you generated in HMS 2) import from your own key management service 3) have the key material generated and used in a AWS CloudHSM cluster
- control permissions by 1) key policy 2) IAM policies with key policy 3) use grants with the key policies
- KMS shared tenancy, automatic key generation and rotation
- CloudHSM dedicated to you and you have full control over hardware, no key rotation

