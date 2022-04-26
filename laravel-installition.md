# installing-laravel-on-linux-OS
i will guide you for installing step by step laravel on linux OS
#############
###########
########
######
####
##
#

hi guys i was trying to install and run laravell V9 on my kali linux and it take long time to me and i decide to discription step by step for every one want to install it fastly. let us get started.

at first you must have php on your linux.
you can download it with this code on your terminal:



#######     
sudo apt-get update     
sudo apt install php
#######



then you must download a softwere named composer.
it's necessary for geting larvel
run the following script in your terminal:




########
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '906a84df04cea2aa72f40b5f787e49f22d4c2f19492ac310e8cba5b96ac8b64115ac402c8cd292b8a03482574915d1a8') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
############################

in next step you must move composer.phar in /usr/local/bin/composer directory

composer.phar is available in curent directory of your terminal that you entered pervious script

#########
sudo mv composer.phar /usr/local/bin/composer
#########

then you must getting laravel with this script

####
composer global require laravel/installer
####

it's not necessary to import laravel in xampp directory you can create a folder on your Desktop
now you most run this script step by step in your terminal

first
###
nano ~/.bash_profile 
###
or
###
vim ~/.bash_profile
###
now add this script to the  file is opened
for nano:
###
export PATH=$HOME/.config/composer/vendor/bin:$PATH
###
then press ctrl+x and save

for vim:
press i key
ctrl+shift+v for pasting this script:     PATH=$HOME/.config/composer/vendor/bin:$PATH
then press esc key
then write :wq! and enter


now run this script in terminal

###
source ~/.bash_profile
###

in next step you can run this code

###
cd ~/Desktop
laravel new laravel
###

that second laravel is your project name

then run this script

####
sudo apt install php-xml
sudo apt-get install php-mbstring
sudo apt-get install php-curl
sudo composer update
###

it's it.
now go to your project folder named laravel and do this

###
cd ~/Desktop/laravel
php artisan serve
###

now you can see your localhost:8000 in your browser
you must add the project folder in your ide
that's it.




