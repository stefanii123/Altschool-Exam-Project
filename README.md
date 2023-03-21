# AltSchool-3rd-Semester-Examination

Steps to deploy your portfolio:
1. Build docker image of your portfolio application. 
2. Push the built docker image of your application to dockerhub. If you don't have an account on dockerhub, create one first. 
3. Build the infrastructure needed to deploy the applications on aws cluster. For this, you'll need to use terraform. So use terraform to create a vpc, internet gateway, nat gateway, route tables and routes, subnet, roles, security group, cluster and node group. 
4. Deploy the applications (portfolio and socks shop) to the cluster created in the previous steps. Use kubernetes to deploy them. 
5. Setup subdomain for the applications using route 53. Remember to include the 8 nameservers from the two subdomain records in your namecheap DNS configuration. 
6. Setup Prometheus and grafana for monitoring the applications. 
7. Create a ci cd pipeline that will:
A. Build and push the portfolio image to dockerhub
B. Deploy the aws infrastructure using terraform
C. Deploy the applications using terraform
D. Deploy the monitoring configuration using terraform
