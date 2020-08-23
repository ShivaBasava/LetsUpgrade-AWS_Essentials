# A README file for Assignment/Project Day4

## Following are the steps-
## Creating & Hosting a Webpage on AWS EC2 Instance(Linux AMI)

- PDF named 'Day-4 Assignment': contains the Use Case/Question for Assignment/Project which is provided by the instructor at LetsUpgrade.
- This Day4 folder of my repository contains the implemented Solution/Answer for the above Use Case/Question in the form of Screenshots.
- Launch two AWS EC2 Instances(Linux AMI) from AWS Management console.
- Login to each AWS EC2 Instance(Linux AMI) by using Putty/Mobaxterm.
- Following are the series of steps to host a Webpage on each Instance:-
    - Swith to the SUPER USER mode by entering this command, sudo su
    - After which, Install httpd service by entering this command, yum install httpd
    - Then change the directory by entering this command, cd /var/www/html
    - Now we have to design our index.html using vi(or nano or Vim) editor by entering this command, vi index.html
    - Save & Exit from the vi editor, esc :wq
    - We have to start the service httpd by entering this command, systemctl start httpd 
    - Hurray! Now our webpage is hosted on AWS EC2 of Linux Instance. Just to verify, Get your respective Public IP of AWS EC2 Instances(Linux AMI) and paste that in browser.

## Creating AWS Elastic Load Balancer

- Following are the steps to create AWS Elastic Load Balancer:-
    - Navigate to Load Balancer from AWS Management console.
    - Select 'Application Load Balancer' HTTP/HTTPS type Load Balancer.
    - Name the Load Balancer and Select:
        - Scheme as 'Internet facing'
        - IP address type as 'IPV4'
        - Load Balancer Protocol as 'HTTP' with PORT '80'
        - Minimum Two Availability Zones
    - Click on Configure Security Groups and provide respective details.
    - Under Configure Routing:
        - Name the Target Group 
        - Target Type as 'Instance'
        - Protocol is HTTP with PORT 80.
    - Now click on Register Targets:
        - Select the Created Linux Instances(from above steps) and click Review and Create.
- Finally copy the DNS name of created Load balancer and enter the same in browser.
