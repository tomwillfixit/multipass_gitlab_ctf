# multipass_gitlab_ctf

Running [GitLab Capture the Flag](https://about.gitlab.com/blog/2020/08/12/how-to-play-gitlab-ctf-at-home/) using Multipass.

# Install Multipass 

Instructions can be found [here](https://multipass.run).

# Launch the VM and start the Containers
```
multipass launch --mem 4G --cpus 4 --disk 10G --cloud-init capture_the_flag.yml --name ctf 20.04
```
You'll see this error but it can be ignored :
```
launch failed: The following errors occurred:                                   
timed out waiting for initialization to complete
```
The cloud init has a default timeout of 5 minutes and pulling the images takes longer than 5 mins.

# Login to VM
```
multipass shell ctf

Follow the progress of cloud init :

sudo tail -f /var/log/cloud-init-output.log

```
# Update /etc/hosts

Add VM IP (found by running multipass ls) and the host : capture.local.thetanuki.io to /etc/hosts.

