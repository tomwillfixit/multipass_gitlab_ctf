# multipass_gitlab_ctf

Running [GitLab Capture the Flag](https://about.gitlab.com/blog/2020/08/12/how-to-play-gitlab-ctf-at-home/) using Multipass.

# Install Multipass 

Instructions can be found [here](https://multipass.run)

# Launch the VM and start the Containers

multipass launch --mem 4G --cpus 4 --disk 10G --cloud-init capture_the_flag.yml --name ctf 20.04

# Login to VM

multipass shell ctf

# Update /etc/hosts

Add VM IP (found by running multipass ls) and the host : capture.local.thetanuki.io to /etc/hosts.

