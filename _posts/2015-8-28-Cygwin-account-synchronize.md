---
layout: post
title: Cygwin account synchronize
---
mkpasswd -l -g > /etc/passwd

mkpasswd -d -u \`whoami\` >> /etc/passwd

mkgroup  -l -u > /etc/group
