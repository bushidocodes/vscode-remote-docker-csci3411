# vscode-remote-docker-csci3411
A project that uses Docker, VSCode, and the Remote Docker extension to automatically configure the CSCI3411 build environment.

## Installation Instructions
1. Install Docker for your appropriate environment.
1. Install Visual Studio Code
1. Install the Remote - Containers Extension
1. git clone https://github.com/bushidocodes/vscode-remote-docker-csci3411.git
1. cd vscode-remote-docker-csci3411
1. code .
1. When you receive a popup stating that VSCode has detected a Remote - Containers configuration and asking if you would like to open this directory in the container, click yes.
1. Be patient while the Docker build image is configured
1. When complete, opening a VSCode terminal will automatically open in the context of the build container
1. Confirm that you can build the Hello World C code as expected.

## Attributions
Based on Microsoft's example VSCode Docker Remote CPP project, which is available under the MIT license.
Modified to align to the tools installed in the Vagrant project at https://github.com/gparmer/OS-standard-env/blob/master/provision.sh
