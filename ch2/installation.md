# Install Node.js and Particle CLI

Node.js is an incredible platform that allows you to build things in javascript, which we will need in order to download and use the Particle CLI (Command Line Interface) which is the way you will be interacting with your hardware (Particle Core) to program your robot.

Depending on the operating system, you will need to follow specific directions, but generally you will:

1. Install [NodeJS](http://nodejs.org) (Click Install)

 Once Node.js is installed, you will also have available the Node Package Manager which is how you will install libraries and utilities that help you build and interact with your hardware/software.

2. Then install the Particle CLI

The Particle Command Line Interface is a tool written by the folks who also made your device.  This tool allows you to connect, claim, and use your device, so you'll need to install it:

```
git clone git@github.com:spark/particle-cli.git
cd particle-cli
npm i . -g
```

3. To make sure that the installation worked, go ahead and try to login to your particle account by typing `particle login` (this will prompt you for your username and password.)  This will actually create an account on particle.io which will allow you to manage your devices. [see Particle Setup](./particleSetup.md)

### For Windows Users

> For windows users you may want to follow these instructions: https://community.particle.io/t/tutorial-particle-cli-on-windows-07-jun-2015/3112

### For Ubuntu Users
> For ubuntu users you may want to follow these instructions: https://community.particle.io/t/how-to-install-the-spark-toolchain-in-ubuntu-14-04/4139
