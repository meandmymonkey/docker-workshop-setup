This is the setup for my docker workshop at PHPNW14.


## Requirements

For the workshop, you should come equipped with:

- A laptop
- A current version of [Vagrant](http://www.vagrantup.com/) (tested with 1.6.5)
- A current version of [Virtualbox](https://www.virtualbox.org/) (tested with 4.3.16)
- Being able to connect to vagrant boxes through SSH - if you are using Windows, you may need something like PuTTy for this
- Basic knowledge how to operate the above, and some Linux shell commands


## Preparation

To make us mostly independent from conference WIFI (part of the workshop
involves installing quite a few Ubuntu packages), we will use two
prepared VMs for the workshop.

Here is how to set these up:

### 1) Get the code

    $ git clone git@github.com:meandmymonkey/docker-workshop-setup.git
    $ cd docker-workshop-setup
    
### 2) Run the boxes

    $ vagrant up
    
### 3) Wait

Vagrant should download and spin up two boxes. These are quite large,
so please be patient.


## Alternative #1

If you have problems with the download during ```vagrant up```, you might want
to get the box files manually and then add them to your host. Between steps #1
and #2 above, please download both boxes from

- http://static.inputrequired.org/phpnw14/phpnw14-services.box
- http://static.inputrequired.org/phpnw14/phpnw14-playground.box

Then, manually add the boxes to Vagrant:

    $ vagrant box add --name phpnw14-services /path/to/phpnw14-services.box
    $ vagrant box add --name phpnw14-playground /path/to/phpnw14-playground.box

After the boxes have been added, continue at step #2.

## Alternative #2

I will bring the box files to the workshop on USB drives as a backup solution.
**However**, every single developer with a ready-to-go setup will speed up the
workshop for everyone else, so please try to download and install the
everything beforehand. Please note you will still need both Vagrant and Virtualbox
ready to go.
