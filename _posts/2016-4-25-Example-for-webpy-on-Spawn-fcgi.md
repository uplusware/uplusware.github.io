---
layout: post
title: Example for webpy on Spawn-fcgi
---
### Webpy Code
	import web
	urls = ("/.*", "hello")
	app = web.application(urls, globals())

	class hello: 
		def GET(self):
			return 'Hello, GET!'

	web.wsgi.runwsgi = lambda func, addr=None: web.wsgi.runfcgi(func, addr)
	if __name__ == "__main__":
		app.run()
    

### Start
<code>sudo spawn-fcgi -d /var/niuhttpd/webpy -f /var/niuhttpd/webpy/main.py -a 127.0.0.1 -p 9001</code>

### Stop
<code>sudo kill `pgrep -f "python /var/niuhttpd/webpy/main.py"`</code>
