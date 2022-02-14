# Installation

Getting started is easy. If you don't have it already, install NodeJS. Then, create an empty folder and do this:

```bash
npm install meshcentral
node node_modules/meshcentral
```

That's it. MeshCentral will set itself up and start managing computers on your local network. By default it will be setup in LAN mode and agents you install will multicast on the local network to find the server. To setup the server so that agents use a well known DNS name and to start customizing your server, go in the "meshcentral-data" folder and edit the config.json file. The configuration file must be valid JSON, you can use this link to validate the file format.

For Windows users, you can download the MeshCentral Installer that will automate installation of NodeJS and provide basic configuration of the server. This option is not recommended for advanced users.

[Win32 MeshCentral Installer](https://meshcentral.com/info/tools/MeshCentralInstaller.exe)

By default, MeshCentral will use NeDB as this is the built-in database. For more advanced users, it's recommended to switch to using MongoDB. MeshCentral can be installed on a very small server. A [Raspberry Pi](https://www.raspberrypi.org/) or [AWS t3.nano running Amazon Linux 2 instance](https://aws.amazon.com/ec2/pricing/on-demand/) for 5$ a month will do just fine for managing up to a few hundred devices.

You can run the MeshCentral Server with --help to get options for background installation.