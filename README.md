# Pros-Ansible
An Ansible script to install pros
## Usage
Install ansible on your computer.
### Debian
Instructions taken from [Ansible Install for Debian](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-debian)

Add the following line to `/etc/apt/sources.list`:

`deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main`

```bash=
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367
sudo apt update
sudo apt install ansible
```
### Ubuntu
Instructions taken from [Ansible Install for Ubuntu](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-ubuntu)
```bash=
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install ansible
```
### Arch
Instructions taken from [Ansible Install for Arch](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-arch-linux)

`sudo pacman -S ansible`
### Fedora
Instructions taken from [Ansible Install for Fedora](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-rhel-centos-or-fedora)

`sudo dnf install ansible`

### Running the playbook
Add `, upload=True` after `user=` if you want the upload alias added.

`sudo ansible-pull -U https://github.com/Sleuth56/Pros-Ansible.git -e "user="`

Logout and back in for the changes to take effect.

## Testing
This is the list of all operating systems that have been or needs tested.
If you run on of these operating systems please give this project a go.
If you do please open an issue with your commands and the console output regardless if it worked or not.
- [ ] Linux
  - [x] Arch
  - [ ] Ubuntu
  - [ ] Debian
  - [ ] Gentoo
  - [ ] Fedora
  - [ ] Suse

Linux is all thats officially supported right now OSX and Windows will be coming soon.
- [ ] OSX
  - [ ] M1
- [ ] Windows


## Developement
- Install ansible.
- `git clone https://github.com/Sleuth56/Pros-Ansible`
- `cd Pros-Ansible`
- `sudo ansible-playbook --connection=local local.yml --check -e "user= , upload=True"`