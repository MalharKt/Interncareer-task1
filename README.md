Firstly, launch an EC2 instance
With the following configuration:

Instance type: t2.medium
Enable the following ports: 3000, 8080, 22, 80
Storage: 10 GB at least
SSH into the instance using the key pair.

Jenkins Setup
Install java : 
sudo apt update
sudo apt install fontconfig openjdk-17-jre
java -version
openjdk version "17.0.8" 2023-07-18
OpenJDK Runtime Environment (build 17.0.8+7-Debian-1deb12u1)
OpenJDK 64-Bit Server VM (build 17.0.8+7-Debian-1deb12u1, mixed mode, sharing)

Install jenkins :
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins

• confugure and access jenkins 
• install required pluggins
• create a pipeline job

Create a Sample Web Application
• Install the necessary dependencies and run the application locally.
• Push it to a GitHub repository.

Jenkins Pipeline Setup
• Clone the Git repository into your instance.
• Create a Jenkins pipeline with stages like build, test, and deploy accordingly.

Install Docker
sudo apt install docker.io -y
docker version

• Integrate Jenkins with GitHub.
• Integrate Jenkins with DockerHub.
• Add a webhook in GitHub.

Automation
Automate all these steps, starting from cloning the repository to running the application using the Jenkins pipeline.

Thank you for following along until now.

😊 HAPPY LEARNING 😊

