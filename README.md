# aws-ec2-nginx-cloudflare
AWS EC2 + Nginx + Cloudflare
Project Overview
I deployed a simple website on an Ubuntu Amazon EC2 instance, configured Nginx to serve a custom webpage, connected a domain through Cloudflare, and enabled HTTPS using Certbot and Let’s Encrypt.

Live site: https://www.zakchoudhury.co.uk

Technologies Used
AWS EC2
Ubuntu Linux
Nginx
Cloudflare DNS
Certbot
Let’s Encrypt
HTML
Architecture
An Ubuntu EC2 instance hosts the website.
Nginx serves the webpage from /var/www/html.
Cloudflare DNS points www.zakchoudhury.co.uk to the EC2 public IPv4 address.
Certbot installs a Let’s Encrypt certificate and configures HTTPS for the www domain.
What I Did
1. Launched an EC2 Instance
Created an EC2 instance running Ubuntu.
Connected to the instance using SSH.
2. Installed and Checked Nginx
Updated the Ubuntu package list.
Installed Nginx.
Verified that Nginx was running and listening on port 80.
3. Configured Cloudflare DNS
Created an A record for www pointing to the EC2 public IPv4 address.
Used Cloudflare to manage the domain’s DNS settings.
4. Enabled HTTPS
Added an inbound HTTPS rule for TCP port 443 in the EC2 security group.
Installed Certbot and its Nginx plugin.
Used Certbot to install the existing Let’s Encrypt certificate for www.zakchoudhury.co.uk.
Verified that the website loaded over HTTPS.
5. Created a Custom Webpage
Created a custom HTML page at:

/var/www/html/index.html

The page displays a welcome message and identifies the project as a website hosted on EC2 using Nginx.

Verification
Confirmed Nginx responded successfully over HTTP.
Confirmed the domain returned an HTTP success response.
Confirmed the website loaded over HTTPS and displayed the custom webpage.
Notes
Ping did not receive replies from the EC2 public IP. This did not prevent the website from working: ping uses ICMP, while the website uses HTTP and HTTPS.

What I Learned
How to launch and connect to an Ubuntu EC2 instance.
How to install and verify Nginx.
How DNS connects a domain to a server.
How EC2 security group rules control inbound traffic.
How to configure HTTPS with Certbot and Let’s Encrypt.
How to publish a custom HTML webpage.
