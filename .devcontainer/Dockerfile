FROM ubuntu:18.04

# Or your actual UID, GID on Linux if not the default 1000
ARG DEBIAN_FRONTEND=noninteractive
ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID

# Update to make sure we have the latest packages
RUN apt-get -y update \
  # Tools for making projects
  && apt-get -y install make cmake \
  # A few useful tools
  && apt-get -y install bc gcc-multilib binutils-dev g++ grep curl build-essential \
  # Useful debugging tools
  && apt-get -y install systemtap \
  # Useful general purpose tools
  && apt-get -y install git ntp \
  # Create a non-root user to use if preferred - see https://aka.ms/vscode-remote/containers/non-root-user.
  && groupadd --gid $USER_GID $USERNAME \
  && useradd -s /bin/bash --uid $USER_UID --gid $USER_GID -m $USERNAME \
  # [Optional] Add sudo support for non-root user
  && apt-get install -y sudo \
  && echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
  && chmod 0440 /etc/sudoers.d/$USERNAME \
  # Cleanup
  && apt-get -y autoremove \
  && apt-get clean -y

