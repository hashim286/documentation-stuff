1. make SSH config file in (your user)/.ssh/ called "config", path to file should look like below

		C:/User/Bob/.ssh/config

2. with a text editor, write in the hostname followed by the parameters you want to save

		Host (hostname/ip)
			User "(username)"

3. to connect, use ssh (hostname/ip), this also works with sftp and scp 

		ssh (hostname/ip)
		scp (path to file) (hostname/ip):(path )
		sftp (hostname/ip)