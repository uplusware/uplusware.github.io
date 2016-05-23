---
layout: post
title: Socket Call Stack - socket
---
	int socket(int domain, int type, int protocol);
		SYSCALL_DEFINE3(socket, int, family, int, type, int, protocol)
			int sock_create(int family, int type, int protocol, struct socket **res)
				int __sock_create(struct net *net, int family, int type, int protocol, struct socket **res, int kern)
					int security_socket_create(int family, int type, int protocol, int kern)
			static int sock_map_fd(struct socket *sock, int flags)
				int get_unused_fd_flags(unsigned flags)
					int __alloc_fd(struct files_struct *files, unsigned start, unsigned end, unsigned flags)
				struct file *sock_alloc_file(struct socket *sock, int flags, const char *dname)
				void put_unused_fd(unsigned int fd)
