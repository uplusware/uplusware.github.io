---
layout: post
title: Socket Call Stack
---

### Socket Call Stack

<pre><code>
#include <sys/socket.h>
int socket(int domain, int type, int protocol);
    SYSCALL_DEFINE3(socket, int, family, int, type, int, protocol)
</code></pre>
