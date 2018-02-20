![Florida Polytechnic University](https://floridapoly.edu/wp-content/themes/floridapolytechnic/images/home_logo.png)
# Local Development Environments Utilizing Virtual Machines
## Introduction to Parallel and Distributed Computing

### Required Software
In order to run the local development box, both Vagrant and Virtual Box are required. You may find the downloads available below.
1. Virtualbox
  * https://www.virtualbox.org/wiki/Downloads
2. Vagrant
  * https://vagrantup.Computer

### Cloning the Repository
In order to get the configuration files required you must either clone this repository or download the zip file from above,

To clone the repository use:
```
git clone https://github.com/dvigne/insert_later
```

### Configuring the box
We are going to map a shared folder between your host and the guest operating system. In order to create the folder structure required run the init scripts below:

For Windows:
```
init.bat
```
For Linux/Mac:
```
./init.sh
```
After running the init scripts you must uncomment a line in the `.VagrantFile`. Open this file in your favorite text editor and find the lines below:
```
# Share an additional folder to the guest VM. The first argument is
# the path on the host to the actual folder. The second argument is
# the path on the guest to mount the folder. And the optional third
# argument is a set of non-required options.
# config.vm.synced_folder "../data", "/vagrant_data"

# Uncomment the line below for Windows:
# config.vm.synced_folder "%userprofile%/documents/Code", "/home/vagrant/Code"

# Uncomment the line below for Linux or Mac:
# config.vm.synced_folder "~/Documents/Code", "/home/vagrant/Code"
```
Uncomment the line that corresponds to your operating system

### Turning on the Lights
After you have those files configured go ahead and turn the virtual machine on with:
```
vagrant up
```
and then connect with:
```
vagrant ssh
```
### Profit
After performing the above, you should have access to a shared folder located at `~/Documents/Code` where you should copy your homework/code that will be kept in sync with the virtual machine!