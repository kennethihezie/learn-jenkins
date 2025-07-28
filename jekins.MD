# Installing jekins on ubumtu

1: sudo apt update -y
2: sudo apt install openjdk-21-jdk
3: sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
4: sudo systemctl start jenkins
5: systemctl status jenkins

http://172.20.10.2:8080/ or http://<server-ip>:8080


Ensure to always backup $JENKINS_HOME folder as it contains very sensitive files like config folder and jobs folders