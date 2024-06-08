# EC2-Backup-and-Restore
#### EC2 Backup and Restore is crucial for ensuring data protection, business continuity, and compliance. Backups prevent data loss, enable quick recovery from failures, and minimize downtime. In addition, backup/restore support disaster recovery, safeguard against threats like ransomware, and facilitate testing. 

## Step 1: Create an EC2 instance 
#### Create an EC2 instance or choose a prepared instance you would like to backup. We will be using instance `TEST-Public` as the the backup instance. 

![IMAGE](https://github.com/ericincloud/EC2-Backup-and-Restore/blob/main/EC2Test-1.JPG)

## Step 2: SSH/Connect into Backup instance
#### Connect to the instance using SSH or an alternative method. Use command `ssh -i your-key.pem ec2-user@your-instance-ip` or the PuTTY application to SSH. 

## Step 3: Create a new file (Optional)
#### Create a new file `example.txt` using the nano text editor. Use command `touch example.txt` to create the file then command `nano example.txt` to edit and type something in! Press `CTRL + X` then `Y` to save. If done correctly, you can view the text you entered by using command `cat example.txt`.

![IMAGE](https://github.com/ericincloud/EC2-Backup-and-Restore/blob/main/EC2TestNano.JPG)

## Step 4: Create EC2 Image
#### Next, select the backup instance then go to `Actions` > `Images and templates` > `Create image`.

![IMAGE](https://github.com/ericincloud/EC2-Backup-and-Restore/blob/main/CreateEC2Image.JPG)

## Step 4: Launch and restore using EC2 Image
#### Head over the the left tab and select `AMIs` under Images. Select the image created from the backup instance then select `Launch instance from AMI`

![IMAGE](https://github.com/ericincloud/EC2-Backup-and-Restore/blob/main/LaunchImage.JPG)

## Step 5: Verify restoration
#### To verify if the backup instance was successfuly restored, SSH into the new instance created from the backup instance. Then use command: `cat example.txt` to view the file and its contents. 

#### Congratulations! You've successfully backed-up and restored an EC2 instance!
![IMAGE](https://github.com/ericincloud/EC2-Backup-and-Restore/blob/main/Restored-EC2.JPG)

## Notes
#### When using Instance Connect, connect as `ec2-user`.

## Reference
#### SSH command: `ssh -i your-key.pem ec2-user@your-instance-ip`
#### Create file: `touch example.txt`
#### Edit file: `nano example.txt`
#### List files: `ls -l`




