## Purpose

1. Create ECR, by terraform

   --> myapp-repository-URL = "530636435709.dkr.ecr.ap-southeast-1.amazonaws.com/myapp"

2. Create Docker image on local repo, first change into \dockerfile dir,next start Docker desktop

   $ docker build -t <URL>:1 .

3. Log local computer into ECR

   $ aws ecr get-login-password --region ap-southeast-1 | docker login --username AWS --password-stdin 530636435709.dkr.ecr.ap-southeast-1.amazonaws.com

4. Push the above Docker image to ECR

   $ docker push <URL>:1
