# My Portfolio
Created a web application using web programming languages. Deployed it on AWS EC2, configured security groups and ensured online accessibility. Mobaxterm is used for running the EC2 virtual server along with github repository for accessing the web application.

## Concepts and frameworks used:-
1. #HTML, CSS and Basic JavaScript# -> <u>"HTML (Hypertext Markup Language)"</u> is the standard language used to create the structure of web pages. It defines the elements like headings, paragraphs, images, and links, essentially providing the skeleton for a website. "CSS (Cascading Style Sheets)" is used to control the visual presentation of a webpage, such as layout, colors, fonts, and spacing. It enhances the appearance, ensuring that the page looks aesthetically appealing and responsive across different devices. "JavaScript" is a programming language that enables interactive features on a website. It adds dynamic functionality like form validation, content updates, animations, and event handling.
  
2. #Amazon AWS EC2# -> <u>"AWS EC2 (Elastic Compute Cloud)"</u> is a web service that provides resizable compute capacity in the cloud. It allows users to launch and manage virtual servers, called instances, which can run a variety of operating systems. EC2 offers scalability, flexibility, and control over the computing environment, allowing businesses and developers to avoid the upfront costs and complexity of owning physical servers. It is commonly used for hosting websites and web applications, running large-scale data processing.
   
3. #Mobaxterm# -> <u>"MobaXterm"</u> is widely used by developers and system administrators for remote system management, network monitoring, and accessing multiple servers simultaneously from a single interface. t offers a range of features such as an SSH client, X11 server, remote desktop (RDP, VNC), file transfer (SFTP, SCP), and a built-in terminal with Unix commands.
   
4. #GitHub# -> <u>"GitHub"</u> is a web-based platform for version control and collaborative software development. It uses Git, a distributed version control system, to track changes in code and manage multiple versions of a project. GitHub allows developers to collaborate by hosting repositories, where they can contribute, review, and merge code changes.

## Steps followed:-
1. Create the EC2 instance
![1](https://github.com/user-attachments/assets/4c1b586b-875f-41a0-8db6-7a11885fef1b)
![2](https://github.com/user-attachments/assets/e15c572d-c74f-41ff-b3e0-80f9baac2bd3)
2. Configure the security groups
![4](https://github.com/user-attachments/assets/b12fa515-bc76-4af1-9c03-e6107475a9f9)
3. Use Mobaxterm for connecting to EC2 instance using the SSH public key
![3](https://github.com/user-attachments/assets/48dfd02a-625c-4a7c-b145-9cf29b1bf085)
4. After conneting to instance, you will get the above interface.
5. Become a root user using the following command.
   #sudo su#
6. Update the required packages and install "httpd" framework along with "git" framework.
   #yum update -y#
   #yum install httpd -y#
   #yum install git -y#
7. Start the httpd using the following commands.
   #sudo syatemctl service start httpd#
You cam also check the status whether httpd is started or not using the following commands.
   #sudo systemctl status httpd#
8. Now go to the html folder which is by deafult created in your instance
   #cd /var/www/html/#
9. Clone your github repository where the portfolio is stored, use the following command
   #git clone <HTTPS link of your repo>#
10. Its done, access your website -> Open your browser and visit your EC2 instance’s public IP address. Your website from GitHub should now be live!
