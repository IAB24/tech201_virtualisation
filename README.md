# DevOps and Development Environments

## DevOps

Responsible for tying teams together in software engineering lifecycle. Shared responsibility.

CLOUD
- engine of internet
- very secure (google datacenter)
- protecting user info very important
- warm 80F helps with efficiency
- overhead power distribution
- custom server rack that can be optimised for high speed computing
- drives destroyed if unreliable
- cool water through coils, keep datacenter cool.

4 areas to improve dev ops
- Ease of use:
Other teams wont use the tools we create if they aren't user friendly. If devs do not use our tools there will be headaches and delays in deployment down the line.

- Flexibility:
It can be wasy to get locked in to using a specific product, tool or software. Makes it harder for the company to keep up with industry changes.
Everything should be easy to change and update if needed for the business.

- Robustness:
We need as close to 100% uptime as possible for our company's services.
We are responsible for achieving this as DevOps engineers.

- Cost:
Cost is often overlooked. We need to make sure the company is being as efficient as possibe in it's tech dealings.
For example how powerful a machine fow we need to conduct a task. Do we need certain servers running?etc.

Monoliths - not flexible/or robust

- Risk register:
Highlights risks in system. Outlines potential damages, chance of occurence and risk to business. 


### Development environments
- Space with all the tools and configurations to run and test programs.

- Increases dev team collaboration.

What makes a good dev environment?
- User friendly, fast and robust
- Should be easy to update
- It should match the production environment as closely as possible
- Acessibility. It should be the same for everyone, everywhere. 
- It should support one application - app1 requires version 1.1 - app 2 needs 1.4 
or app1 conflicts with a program app2 needs.


- Virtualisation allows you to set up a dev environment equal for everyone using VMs.

### Tooling/settings

How to set up ruby:
https://rubyinstaller.org/downloads/

How to set up virtual box:
https://www.virtualbox.org/wiki/Download_Old_Builds_6_1

How to set up vagrant:
https://www.vagrantup.com/

Windows hypervisor on


### Vagrant
Create a directory for your project and navigate to it in the terminal.

Initialize the project with a specific base image by running the command vagrant init ubuntu/xenial64. This will create a Vagrantfile in the directory, which is used to configure your virtual environment.

Vagrant file has this code in it in ruby. You will need to delete the comments.

```
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"


end
```

Start the virtual machine by running the command vagrant up.

Connect to the virtual machine by running vagrant ssh.

ls -a shows hidden files 

sudo apt get update -y

sudo apt-get install nginx -y

sudo systemctl start nginx

sudo systemctl status nginx

```
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.10.100"


end
```
exit using ctrl c

vagrant reload

type.ip address into browser and you can see these changes have been made.

VMs - emulating an operating system within your own OS

## Advanced Bash

uname - OS system

- Flags (-y, -a, -s, -r etc.) modify operations. also called options

- cd change directory
/ root, ~ home

ls list files, tells you where you are.

relative path where is it from me
/Folder1/Folder2

absolute path where is it from root
C:\users\username\Documents\myfile.txt
https://www.mysite.com/myfolder/subfolder/sub/sub2page1.html

touch - create file
touch emptyfile.txt

nano makes file/opens editor in linux
cat- prints changes in nano

mkdir new file
cp copy contents of file into another file

r - recursive, everything in folder
rsync synchronise files
mv move files
move file several files down ex mv myfile.txt/../../exfile.txt
you can rename files too
my_file2.txt

rm- remove files - no check so be careful (rm-rf deletes everything)
man ls
man -k change (keyword) brings up  docs with keyword in it
grep test find where keywords are in files
grep test * -R recursive search
wildcards are used to match multiple filenames or pattern of characters, such as * (matches any number of characters) or ? (matches exactly one character). They are used in bash commands, such as ls or rm, to operate on multiple files at once.

VM terminal is not colourful unlike PC

