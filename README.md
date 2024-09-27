Setup Continuous Integration/Continuous
Deployment (CI/CD) Pipeline

Step 1: Launch EC2 Instance
Launch an EC2 instance with the following configuration:
• Instance Type: t2.medium
• Enabled Ports: 3000, 8080, 22, 80
• Storage: At least 10 GB
SSH into the instance using the key pair.

Step 2: Jenkins Setup
Install Java
Update the package list and install Java:
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

• Configure and access Jenkins through the web interface.
• Install the required plugins.
• Create a pipeline job.

Step 3: Create a Sample Web Application
• Create a sample web application.
• Install the dependencies and run it locally.
• Push the code to a GitHub repository.

Step 4: Jenkins Pipeline Setup
• Clone the Git repository into your instance.
• Create a Jenkins pipeline with stages like build, test, and deploy accordingly.

Step 5: Install Docker
Install Docker on your EC2 instance:
sudo apt install docker.io -y
docker version

Build the Docker image from the cloned repository using the following command:
docker build -t <image-name> .

Run the Docker image using:
docker run -d -p portno:portno <image-name>

Access the application via http://<ec2-public-ip>:8080

Step 6: Integrate Jenkins
• Integrate Jenkins with GitHub by connecting your repository.
• Integrate Jenkins with DockerHub to push Docker images automatically.
• Add a webhook in GitHub to trigger Jenkins builds on code changes.

Step 7: Automate the Pipeline
Automate the entire process from:

• Cloning the repository.
• Building the application.
• Running the Docker container.
• Deploying the application, all through the Jenkins pipeline.

Thank you for following along! 😊

🎉 Happy Learning! 🎉

