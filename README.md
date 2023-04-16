# Jenkins-installation-easy-step
Installing Jenkins on Ubuntu

create an instance in AWS
![image](https://user-images.githubusercontent.com/114645192/232275131-1a95aeef-3d6b-462d-88f8-d4bd46966dce.png)

update your instance:

sudo apt-get update

![image](https://user-images.githubusercontent.com/114645192/232275164-e10499b5-8988-44ca-8b43-4e77e51c1d6a.png)

install java:
sudo apt install openjdk-11-jre

To check the version of java on your system, use the following command:

java -version

![image](https://user-images.githubusercontent.com/114645192/232275191-b518120d-6b9a-4087-b016-6b0f64ff20f0.png)

Step 1 — Installing Jenkins
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
  
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
  
sudo apt-get update
sudo apt-get install jenkins

Step 2 — Starting Jenkins

now that Jenkins is installed, start it by using systemctl:

sudo systemctl start jenkins.service

Since systemctl doesn’t display status output, we’ll use the status command to verify that Jenkins started successfully:

sudo systemctl status jenkins

Note:Open port 8080 in the inbound traffic rules as show below.

EC2 > Instances > Click on
In the bottom tabs -> Click on Security
Security groups
Add inbound traffic rules as shown in the image (you can just allow TCP 8080 as well, in my case, I allowed All traffic).
![image](https://user-images.githubusercontent.com/114645192/232275292-48aaa1c8-5509-43d8-9b70-cdb6d0d2dcbb.png)


![image](https://user-images.githubusercontent.com/114645192/232275392-92b15b0d-82cc-4d0d-8f74-c80915ae36df.png)
go to your terminal

sudo cat /var/lib/jenkins/secrets/initialadminpassword
![image](https://user-images.githubusercontent.com/114645192/232275469-18343b8c-512e-4f10-8d36-c59308664530.png)
copy this password: 9f48d46e86a443d7b5171e45cef18f2d

and paste it here.

![image](https://user-images.githubusercontent.com/114645192/232275569-877b8354-d39d-4f6d-9a26-0721fa35bbd8.png)

![image](https://user-images.githubusercontent.com/114645192/232275602-a87c85e2-cb60-4712-8422-acc10140ef71.png)

![image](https://user-images.githubusercontent.com/114645192/232275639-25f8b6a0-5b04-4b16-91d6-64af385dd946.png)

![image](https://user-images.githubusercontent.com/114645192/232275672-c1488e0c-a553-4384-8468-00a293b56ab8.png)

![image](https://user-images.githubusercontent.com/114645192/232275698-2e857620-5ece-49f1-be9d-60b18e36660b.png)

![image](https://user-images.githubusercontent.com/114645192/232275725-082dfae9-e986-4da0-9bec-fec1338cff8e.png)

![image](https://user-images.githubusercontent.com/114645192/232275766-45688ad2-a67f-4d98-9682-a6d8055027bb.png)
