<<<<<<< HEAD
Blackfire + Magento Vagrant
======================

Based on https://github.com/r-baker/simple-magento-vagrant, but with the Blackfire profiler added and configured for you.

Includes https://github.com/magento-hackathon/Blackfireio

See the 'Prerequisites' section for important steps to launch Blackfire

A VERY simple Magento environment provisioner for [Vagrant](http://www.vagrantup.com/), with the Blackfire profiler included.

![Magento & Vagrant](https://cookieflow.files.wordpress.com/2013/07/magento_vagrant.jpg?w=525&h=225)

* Creates a running Magento development environment with a few simple commands.
* Runs on Ubuntu (Trusty 14.04 64 Bit) \w PHP 5.5, MySQL 5.5, Apache 2.2
* Uses [Magento CE 1.9.1.0](http://www.magentocommerce.com/download)
* Automatically runs Magento's installer and creates CMS admin account.
* Optionally installs Magento Sample Store Inventory
* Automatically runs [n98-magerun](https://github.com/netz98/n98-magerun) installer.
* Perfect for rapid development or extension testing with an unopionionated, bare-bones and easily tweaked configuration.
* Goes from naught-to-Magento in a couple of minutes.

## Getting Started

**Prerequisites**

* Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
* Install [Vagrant](http://www.vagrantup.com/)
* Clone or [download](https://github.com/joshuaswarren/BlackfireMagentoVagrant/archive/master.zip) this repository to the root of your project directory `git clone https://github.com/joshuaswarren/BlackfireMagentoVagrant.git`
* Setup a free [Blackfire account](https://blackfire.io/)
* Obtain your Server Id, Server Token, Client Id and Client Token from your [Blackfire Account](https://blackfire.io/account/credentials)
* Edit bootstrap.sh and replace the placeholder text near the bottom of the file with your Blackfire Credentials.
* Install the Blackfire Companion in Google Chrome from the [Chrome Web Store](https://chrome.google.com/webstore/detail/blackfire-companion/miefikpgahefdbcgoiicnmpbeeomffld?hl=en)
* In your project directory, run `vagrant up`

The first time you run this, Vagrant will download the bare Ubuntu box image. This can take a little while as the image is a few-hundred Mb. This is only performed once.

Vagrant will configure the base system before downloading Magento and running the installer.

## Usage

* In your browser, head to `127.0.0.1:8080`
* In the Chrome toolbar, click the Blackfire icon, choose an empty profile slot and click 'Profile' to profile the current page.
* To enable the Blackfire Hackathon extension to provide more refined results, login to the admin panel and set Advanced -> Developer -> Debug -> Profiler to 'Yes' on the global scope.
* Magento admin panel is accessed at `127.0.0.1:8080/admin`
* User: `admin` Password: `password123123`
* Access the virtual machine directly using `vagrant ssh`
* When you're done `vagrant halt`

[Full Vagrant command documentation](http://docs.vagrantup.com/v2/cli/index.html)

## Sample Data

Sample data is automatically downloaded and installed by default. However, it's a reasonably large file and can take a while to download.

> "I don't want sample data"

Sample data installation can be disabled:

 * Open `Vagrantfile`
 * Change `sample_data = "true"` to `sample_data = "false"`
 * Run `vagrant up` as normal

> "I have already downloaded the sample data"

 * Place the sample data `tar.gz` file in the project root
 * Ensure `sample_data = "true"`
 * The provisioning script will skip the download and use the provided file instead. The same goes for when the provisioner is rerun. e.g. `vagrant reload --provision`

## Todo
* Install Modman.

**Why no Puppet/Chef?**
Admittedly, Puppet and Chef are excellent solutions for predictable and documented system configurations. The emphasis for this provisioner is on unopinionated simplicity. There are some excellent Puppet / Chef Magento configurations on Github with far more bells and whistles.
=======
# cleverva
>>>>>>> e0f38cd70c378495c2da165b0682c2f51a5822fc
