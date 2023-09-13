# DevOps

## Jenkins Configuration

1. On Windows
    1. Download jenkins.war file from https://updates.jenkins.io/download/war/.
    2. Ensure installation of java 8 or 11.
    3. Navigate to the war file directory and open cmd.
    4. Run command `java -jar jenkins.war`.
    5. Open web browser on localhost:8080.
    6. Login as admin with password present in ".jenkins\secrets\initialAdminPassword.txt".

2. On Linus/ubantu Machine
    1. Open Terminal and run command `sudo apt-get update`.
    2. Install Java 8 or 11 using command `sudo apt-get -y install openjdk-8-jdk openjdk-8-jre`.
    3. run the following commands to install jenkins in ubantu/debian machine
        `curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
        /usr/share/keyrings/jenkins-keyring.asc > /dev/null`
        `echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
        https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
        /etc/apt/sources.list.d/jenkins.list > /dev/null`
        `sudo apt-get update`
        `sudo apt-get install fontconfig openjdk-11-jre`
        `sudo apt-get install jenkins`
    4. Start Jenkins using `sudo systemctl start jenkins`.
    5. Check status using `sudo systemctl status jenkins`.
    6. Enable Jenkins Auto `sudo systemctl enable jenkins`.
    7. Allow ingress traffic on node port 8080 either via security group, firewall or inbound traffic in Cloud platform. 
    8. open web browser on <ipaddress>:8080