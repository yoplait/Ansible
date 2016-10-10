# Ansible stuff

Ansible and configuration management is the way to do things faster and non-repetitive.
Consistency across the world. And in this case, in different with Chef and Puppet (that I love too) you don’t need an agent!
What makes Ansible special is idempotency, 


You can speak with me:

Mail: 		[https://about.me/perezpardojc](https://about.me/perezpardojc)

Twitter: 	[https://twitter.com/perezpardojc](https://twitter.com/perezpardojc)

curious:	[pepa](pi)


## Non-Idempotent Bash

* `echo "127.0.0.1 localhost" >> /etc/hosts`

## Sample Idempotency Achieved in Bash


* `if (!grep -q 127.0.0.1 /etc/hosts); then echo "127.0.0.1 localhost" >> /etc/hosts; fi`

Thanks!


JC