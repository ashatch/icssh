# icssh

`icssh` either accepts IP address on stdin or as a comma separated list of ip address (no spaces) as an argument.

    Usage:
       icssh [options...] <comma separated ip list>
    Options:
       -u --user        User, default ec2-user
       -s --safe        Default off, enabling safe will prevent connecting to unknown hosts
       -i --identity    SSH key file

Examples:

    echo "127.0.0.1" | icssh -u centos
    icssh -u centos 127.0.0.1,127.0.0.2

In conjunction with [awsip](https://github.com/ashatch/awsip):

    awsip cf my-stack | icssh -u ec2-user


# Prerequisites

The fabulous [iTerm2](https://www.iterm2.com/).

# Installation

Install via brew.

    brew tap ashatch/homebrew-repo
    brew install icssh
