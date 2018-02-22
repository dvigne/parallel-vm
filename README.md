![Florida Polytechnic University](https://floridapoly.edu/wp-content/themes/floridapolytechnic/images/home_logo.png)
# Local Development Environments Utilizing Virtual Machines
## Introduction to Parallel and Distributed Computing

### Required Software
In order to run the local development box, both Vagrant and Virtual Box are required. You may find the downloads available below.
1. Virtualbox
  * https://www.virtualbox.org/wiki/Downloads
2. Vagrant
  * https://vagrantup.com
3. Git SCM
  * https://git-scm.com/downloads

### Cloning the Repository
In order to get the configuration files required you must either clone this repository or download the zip file from above,

To clone the repository use:
```
git clone https://github.com/dvigne/parallel-vm.git && cd parallel-vm
```

### Configuring the box
Once you have cloned the box there will be a `Vagrantfile` for configuring the virtual machine and an `init` script responsible for creating the directory structure required for shared folders between your host computer and the virtual machine.

First download the box:
```
vagrant box add dvigne/parallel-vm
```
Run the init scripts below (optional)

For Windows:
```
init.bat
```
For Linux/Mac:
```
./init.sh
```
### Turning on the Lights
After you have the Vagrant Box Downloaded and shared folders configured go ahead and turn the virtual machine on with:
```
vagrant up
```
and then connect with:
```
vagrant ssh
```
### Profit
After performing the above, you should have access to a shared folder located at the root of the Vagrant Box. You can find the path of the Vagrant folder by typing either `cd` for Windows or `pwd` for Mac/Linux. You may drag your hw/code there to sync files between your virtual machine and host operating system. This allows you to edit in your favorite text editor and your changes will be reflected within the virtual machine to compile and test. Your synced files are located within the virtual machine at `/vagrant`. If you mapped the additional, optional folder, you may also put your code in your hosts `./Code` folder and it will be available under `~/Code` in the virtual machine.

Happy coding! :heart:
