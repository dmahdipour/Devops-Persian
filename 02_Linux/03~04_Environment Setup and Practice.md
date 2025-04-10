
**Note:** It should be automatic. 
One of the best: HashiCorp company:
* Packer -> Preparing Image -> Create ISO image for machine image.
* Vagrant -> Preparing Environment -> Automatic create a virtual OS step-by-step and customized (image, network card, etc.) -> Export as a vagrant file. 
### Install Vagrant:
#### Add the HashiCorp GPG key
Proxy is needed (Can be used in tmux): 
``` bash
ssh -L 9898:localhost:80 -C user@serve
```

```bash
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
```
#### Add the official HashiCorp Linux repository.
```bash
sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
```
#### Update and install.
``` bash
sudo apt-get update
sudo apt-get install vagrant
sudo apt-get install packer
```
#### Add public box in vagrant
##### Adding a bento box to Vagrant
```bash
vagrant box add --provider virtualbox bento/ubuntu-22.04
vagrant box add --provider virtualbox bento/debian-12
```
##### Using a bento box in a Vagrantfile

```bash
Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-20.04"
end
```

``` bash
Vagrant.configure("2") do |config|
  config.vm.box = "bento/debian-12"
end
```
#### Building Boxes
##### Requirements: install packer, vagrant and virtualbox
##### clone bento project
```bash 
git clone https://github.com/chef/bento.git
```
##### To build an Ubuntu 18.04 box for only the VirtualBox provider
```bash
cd packer_templates/ubuntu
packer build -only=virtualbox-iso ubuntu-22.04-amd64.json
```

### See Boxes list
```bash
ls ~/.vagrant.d/boxes
```
