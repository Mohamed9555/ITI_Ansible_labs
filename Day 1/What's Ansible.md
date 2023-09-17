# What's Ansible

Create: 2023-09-14 09:42

- ![[Pasted image 20230914094723.png]]
- tricky question : it's agentless but does it need any specific installment on the client?
	- yes it needs python installed and ssh access
- idempotent: check existing config and if it's same it doesn't do anything 
	- install nginx if it's installed it leaves it and doesn't do anything more 
- to open ssh 
	- start ssh service 
	- to open the port 22 (ssh service listens on port 22)
	- allow specific IP the access the port
	- ![[Pasted image 20230914100631.png]]
	- ssh utility is the client same as docker when you do docker run (client)
		- ![[Pasted image 20230914100935.png]]
		- ssh d = ssh demon (server)
			- ![[Pasted image 20230914101015.png]]
- connecting from pc1 to pc2
	- you don't connect from pc1 to pc2 you actually connect from user to user 
	- ![[Pasted image 20230914102104.png]]
	- so you only act as user (A) and ==it's permissions==
- Another method to connect (public key: private key)
	- ![[Pasted image 20230914102719.png]]
	- public is the locket : private is the key 
- fi aws zy file.pem da bi2ba 2l key pair 2li b connect beh 3l instance 
- using ssh on container 
- ![[Pasted image 20230914110307.png]]
- ![[Pasted image 20230914110539.png]]
- to generate key pair: ssh-keygen -t rsa  
- ![[Pasted image 20230914113832.png]]
- devops.pub + devops.epem
- ssh-copy-id -i devops.pub ansible@172.17.0.2
- ssh -i devops ansible@172.17.0.2 -> using private key devops
## installing Ansible
- sudo apt install ansible 
- ![[Pasted image 20230914120952.png]]
- ![[Pasted image 20230914121207.png]]
- config file
- ![[Pasted image 20230914124940.png]]
- by default it switches on root or sudo 
- ![[Pasted image 20230914130654.png]]
- ![[Pasted image 20230914131005.png]]
- ![[Pasted image 20230914131522.png]]
- ![[Pasted image 20230914132211.png]]
- ![[Pasted image 20230914132602.png]]
# ChatGPT Thoughts
- idempotent
- agentless




# Summary





## Reference
