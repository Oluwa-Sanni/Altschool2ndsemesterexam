1.  I created a AWS account.

2.  I located EC2 while logged in to the AWS account I created.

3.  I changed the region on the AWS account to Cape town.

4.  I created a new Ubuntu instance from EC2 in AWS console, and I
    created new security group to allow inbound connection via http port
    80, ssh via port 22 and https via port 443.

5.  Connected to the created Instance via SSH using the Key pair
    generated.

6.  I then installed NGINX and Git on the running instance:

```{=html}
<!-- -->
```
I.  Sudo apt update

II. Sudo apt install nginx

III. Sudo apt install git-all

```{=html}
<!-- -->
```
7.  I also allowed firewall permission for nginx by running:

```{=html}
<!-- -->
```
I.  Sudo ufw allow 'Nginx Full'

```{=html}
<!-- -->
```
8.  I then created the html document on my vs code

9.  After creating the index.html file I created a github repository on
    my github account named **Altschool2ndsemesterexam**

10. In the folder containing the index.html file I initialized a git
    repo and then pushed to the created repository in github:

```{=html}
<!-- -->
```
II. Git init

III. Git add .

IV. Git commit --m "Second semester exam"

V.  Git remote add origin
    https://github.com/Oluwa-Sanni/Altschool2ndsemesterexam.git

VI. Git push -u origin main

```{=html}
<!-- -->
```
11. After pushing the index.html file to my github repo, I cloned it on
    the instance running by running the command below:

```{=html}
<!-- -->
```
I.  Git clone
    <https://github.com/Oluwa-Sanni/Altschool2ndsemesterexam.git>

```{=html}
<!-- -->
```
12. I copied the index.html file to the /var/www/html directory by the
    query below:

```{=html}
<!-- -->
```
II. Cp index.html /var/www/html

```{=html}
<!-- -->
```
13. I then edited nginx virtual host configuration to read the html.html
    in the directory /var/www/html.

```{=html}
<!-- -->
```
III. sudo vi /etc/nginx/sites-available/default

```{=html}
<!-- -->
```
14. I restarted the nginx web server:

```{=html}
<!-- -->
```
IV. Sudo systemctl restart nginx

CREATED INSTANCE PUBLIC IP: http://13.247.120.129
