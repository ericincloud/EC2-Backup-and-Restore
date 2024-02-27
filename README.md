# EC2-Backup-and-Restore
#### How to backup an EC2 instance and restore it! 
#### In this guide, an example EC2 will be  ..............

## Step 1: Create an EC2 instance (Optional)
#### Create an EC2 instance or choose a prepared instance you would like to backup. We will be using instance `TEST-Public` as the the backup intance. 

![IMAGE]()

## Step 2: SSH/Connect into Backup instance
#### Connect to the Backup instance using SSH or an alternative method. Use command `ssh -i your-key.pem ec2-user@your-instance-ip` or the PuTTY application to SSH. 

![IMAGE]()

## Step 3: Create a new file (Optional)
#### Create a new file `example.txt` using the nano text editor. Use command `touch example.txt` to create the file then command `nano example.txt` to edit - type something in! Press `CTRL + X` then `Y` to save. If done correctly, you can view the text you entered by using command `cat example.txt`.

![IMAGE]()

## Step 4: Create EC2 Image
#### Next, select the backup instance then go to `Actions` > `Images and templates` > `Create image`.

![IMAGE]()
![IMAGE]()

## Step 4: Launch and restore using EC2 Image
#### Head over the the left tab and select `AMIs` under Images. Select the image created from the backup instance then select `Launch instance from AMI`

![IMAGE]()

## Step 5: Verify restoration
#### To verify if the backup instance was successfuly restored, SSH into the new instance created from the backup instance and use command: `cat example.txt` to to view the file and its contents. 

