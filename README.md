# Imanee Sandbox
A Vagrant environment for playing around with Imanee. It's a Ubuntu 14.04 server running Nginx+php5-fpm with PHP version 5.6. Comes with both ``php5-gd`` and ``php5-imagick`` extensions installed.

This is intended to be used by people who don't want to install the PHP image extensions on their own machine or don't have a PHP server installed locally.

## Requirements
You need Vagrant, VirtualBox and Ansible to run this VM.

## Usage
1. Clone this repository
2. Run ``vagrant up``
3. Log in to the server by running ``vagrant ssh``
4. Access the directory ``/vagrant``
5. Initialize the demos submodule with ``git submodule init|git submodule update``
6. Go to the demos folder
7. Run ``composer install``
8. Point your browser to ``192.168.13.99`` and you should see a list of the demos available.

### Troubleshooting

If you get an error at the end of the Vagrant provision, it's ok - I'm not sure yet what's wrong but that's just the "notify" part that restart php5-fpm. You should manually restart by logging in with ``vagrant ssh`` and running ``sudo service php5-fpm restart``

Sorry about that, this sandbox was a last-minute thing and I still didn't have time to fix it :D
