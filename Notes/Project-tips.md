
Amazon linux Jenkins installation 

  1  sudo yum update –y
    2  sudo wget -O /etc/yum.repos.d/jenkins.repo     https://pkg.jenkins.io/redhat-stable/jenkins.repo
    3  sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
    4  sudo yum upgrade
	
    5  sudo dnf install java-17-amazon-corretto -y
    6  sudo yum install jenkins -y
    7  sudo systemctl enable jenkins
    8  sudo systemctl start jenkins
    9  sudo systemctl status jenkins
    38  mkdir jdk
    39  cd jdk/
    40  wget https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz
    43  ll
    43  tar -xzf openjdk-17.0.2_linux-x64_bin.tar.gz
    44  cd jdk-17.0.2/
    45  ll
    46  pwd
    47  cd /home/ec2-user/jdk
    50  sudo mv jdk-17* /usr/lib/jvm/java-17-openjdk/
    51  cd /usr/lib/jvm/java-17-openjdk/
    52  sudo yum install git -y
    53  which git
    54 cd
    55 mkdir maven
    56 wget https://dlcdn.apache.org/maven/maven-3/3.9.9/binaries/apache-maven-3.9.9-bin.tar.gz
    57 tar -xzf apache-maven-3.9.9-bin.tar.gz
    56  sudo mkdir -p /usr/lib/maven/3/
    57  sudo mv apache* /usr/lib/maven/3/
    58  ll /usr/lib/maven/3/apache-maven-3.9.9



 

    http://ec2-54-234-193-71.compute-1.amazonaws.com:8080/login?from=%2F
    
   
    
    Steps to Create a Multi-Branch Pipeline
Configure Credentials in Jenkins:

Navigate to Jenkins Dashboard > Manage Jenkins > Manage Credentials.
Add your GitHub credentials (username and personal access token) for accessing your GitHub repository. Choose "Username with password" and use your GitHub username and the personal access token as the password.
