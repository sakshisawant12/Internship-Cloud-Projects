## Deployment Steps

1. Launch an **AWS EC2 instance** using **Red Hat Enterprise Linux**.

2. Configure the **Security Group**:
   - SSH — Port `22` — My IP
   - HTTP — Port `80` — `0.0.0.0/0`
   - HTTPS — Port `443` — `0.0.0.0/0`

3. Connect to the EC2 instance using SSH:
   `ssh -i web-key.pem ec2-user@<EC2-PUBLIC-IP>`

4. Update the system:
   `sudo dnf update -y`

5. Install Nginx:
   `sudo dnf install nginx -y`

6. Start Nginx:
   `sudo systemctl start nginx`

7. Enable Nginx to start automatically after reboot:
   `sudo systemctl enable nginx`

8. Verify that Nginx is running:
   `sudo systemctl status nginx`

9. Open the EC2 Public IP in a browser to verify the default Nginx webpage:
   `http://<EC2-PUBLIC-IP>`

10. Navigate to the Nginx web directory:
    `cd /usr/share/nginx/html`

11. Install Nano:
    `sudo dnf install nano -y`

12. Create and edit the website file:
    `sudo nano index.html`

13. Add the custom HTML webpage and save the file.

14. Restart Nginx:
    `sudo systemctl restart nginx`

15. Open the EC2 Public IP again in the browser:
    `http://<EC2-PUBLIC-IP>`

16. Verify that the custom website is successfully displayed.
