# Day 2

Create: 2023-09-15 10:07

- ansible web-servers -m ==gather_facts==
	- gathers info about the host (IP, disk, .....)

## Ansible Playbook
- list of plays
- there can be ==one or many plays== in a playbook
- ex:  ansible-playbook iti-playbook.yml (when we have config file)
- can add gather_facts: false to disabled default gather_facts module 
	![[Pasted image 20230915102547.png]]
### Play 
- mapping between a set of hosts (groups, hostnames, or IPs) and the tasks which run on those hosts
- example:
	- name: your play name
		hosts: all
		tasks: 
		- name: your task name 
		  ping: (doesn't take argument)
- we can't see the output if we run the playbook 
- to see it we need to use debug module 
	- save the output in register called x
	- create a new module (task) 
		- why new task cause can't have multiple modules different from each other but they can be the same tho
	- ![[Pasted image 20230915104105.png]]

- ==commands are not impotent what that means?==
	- every time it runs it will make a change no matter what 
- ==x.stdout==
- Play RECAP
- using when and showing skipped ![[Pasted image 20230915105455.png]]
- ![[Pasted image 20230915105702.png]]
	- to avoid ansible failing at this point and continue execution add keyword ==ignore_error: true== after the command ![[Pasted image 20230915105847.png]]
	- ingored = 1 in Play RECAP
- Rescued 
	- ![[Pasted image 20230915110623.png]]
- task 1
	- ![[Pasted image 20230915111636.png]]
## Ansible Modules

- take a look on the requirements when using modules
- task:
	- ![[Pasted image 20230915122709.png]]
	- ![[Pasted image 20230915122833.png]]
	- ![[Pasted image 20230915123207.png]]



## Tags



## Variables


## Loops


## When



## Register 

# ChatGPT Thoughts




# Summary





## Reference
