# EBS Encryption

- EBS Encryption encrypts a volume with a data key using the industry-standard AES-256 algorithm.
- EBS Encryption uses AWS Key Management Service (AWS KMS) customer master keys (CMK) when creating encrypted volumes and snapshots
- Data at rest is encrypted within the volume
- All data moving between the EC2 instance and the volume is encrypted
- All snapshots are encrypted
- All volumes created from snapshots are encrypted
- Encryption and decryption are handled transparently - the user does not need to do anything
- Encryption has minimal impact on latency
- Copying an unencrypted snapshot allows encryption
- Snapshots of encrypted volumes are encrypted
- Root device volumes can be encrypted on creation
