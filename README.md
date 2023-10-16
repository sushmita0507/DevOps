# DevOps

## Jenkins Configuration

1. On Windows
    1. Download jenkins.war file from https://updates.jenkins.io/download/war/.
    2. Ensure installation of java 8 or 11.
    3. Navigate to the war file directory and open cmd.
    4. Run command `java -jar jenkins.war --httpPort={Port_number}`.
    5. Open web browser on ipadress:Port_number or localhost:Port_number.
    6. Login as admin with password present in ".jenkins\secrets\initialAdminPassword.txt".

2. On Linus/ubantu Machine
    1. Open Terminal and run command `sudo apt-get update`.  
    2. Install Java 8 or 11 using command `sudo apt-get -y install openjdk-8-jdk openjdk-8-jre`.  
    3. Follow guideline to install jenkins in ubantu/debian machine from    
        `https://www.jenkins.io/doc/book/installing/linux/#debianubuntu-`
    4. Start Jenkins using `sudo systemctl start jenkins`.
    5. Check status using `sudo systemctl status jenkins`.
    6. Enable Jenkins Auto `sudo systemctl enable jenkins`.
    7. Allow ingress traffic on node port 8080 either via security group, firewall or inbound traffic in Cloud platform. 
    8. open web browser on ipaddress:8080
    