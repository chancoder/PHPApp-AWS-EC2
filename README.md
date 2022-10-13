# PHPApp-AWS-EC2
PHP Sample application on EC2 instance that connect to RDS

# Installation Instruction

1. Launch EC 2 Instane and SSH into it

```
sudo yum update 
```

```
sudo amazon-linux-extras install -y lamp-mariadb10.2-php7.2 php7.2
```

```
sudo yum install -y httpd
```

```
sudo systemctl start httpd
```

```
sudo systemctl enable httpd
```

```
sudo groupadd www
```

```
sudo usermod -a -G www ec2-user
```

```
sudo chgrp -R www /var/www
```

```
sudo chmod 2775 /var/www
find /var/www -type d -exec sudo chmod 2775 {} +
```

```
find /var/www -type f -exec sudo chmod 0664 {} +
```

upload "index.html" to "/var/www/html/" directory
