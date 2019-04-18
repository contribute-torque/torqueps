# TorquePS (forked from Monero Integrations)
A Prestashop addon for accepting Torque (XMR)

Compatible with the stable version of Prestashop (1.6.x). And working on 1.7.x

## Dependencies
This plugin is rather simple but there are a few things that need to be set up beforehand.

* A web server! Ideally with the most recent versions of PHP and mysql

* A Torque wallet. You can find the official wallet [here](https://gettorque.org/downloads/)

* [Prestashop](https://prestashop.com)
Prestashop is open source e-commerce engine to run your own shop and this Torque addon

## Step 1: Activating the plugin
* Downloading: First of all, you will need to download the module. You can download the latest release as a .zip file from https://github.com/contribute-torque/torqueps If you wish, you can also download the latest source code from GitHub. This can be done with the command `git clone https://github.com/torque-integrations/torqueps.git` or can be downloaded as a zip file from the GitHub web page.

* Unzip the file torqueps-master.zip if you downloaded the zip from the master page [here](https://github.com/contribute-torque/torqueps).

* Upload the module and activate it. You can refer the official documentation [here](https://addons.prestashop.com/en/content/21-how-to)

## Step 2 : Use your wallet address and connect to a Torque daemon

### Running a full node yourself

To do this: start the Torque daemon on your server and leave it running in the background. This can be accomplished by running `./torqued` inside your Torque downloads folder. The first time that you start your node, the Torque daemon will download and sync the entire Torque blockchain. This can take several hours and is best done on a machine with at least 4GB of ram, an SSD hard drive (with at least 40GB of free space), and a high speed internet connection.
You can refer the official documentation for running full node from [here](https://github.com/contribute-torque/to

### Setup your Torque wallet-rpc

* Setup a Torque wallet using the torque-wallet-cli tool. If you do not know how to do this you can learn about it at [https://github.com/contribute-torque/torque](https://github.com/contribute-torque/torque)
* Start the Wallet RPC and leave it running in the background. This can be accomplished by running `torque-wallet-rpc --wallet-file /path/to/wallet/file --password walletPassword --rpc-bind-port 20189 --disable-rpc-login` where "/path/to/wallet/file" is the wallet file for your Torque wallet.

## Step 3: Setup Torque Gateway in Prestashop
* Navigate to the "Modules and Services" panel in the Prestashop sidebar and identify `Torque Payments` module and click on `configure`.
* Update `Torque Wallet Address` and `Wallet RPC IP/HOST`
* Note: Wallet RPC IP should start with the protocol and end with port address. `Eg. http://127.0.0.1:20189`
* Save the changes and you are good to go.

## Donating Monero Integrations
XMR Address : `44krVcL6TPkANjpFwS2GWvg1kJhTrN7y9heVeQiDJ3rP8iGbCd5GeA4f3c2NKYHC1R4mCgnW7dsUUUae2m9GiNBGT4T8s2X`
