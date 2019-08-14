
default:	build

clean:
	rm -rf Makefile nginx-1.16.1

build:
	$(MAKE) -f nginx-1.16.1/Makefile

install:
	$(MAKE) -f nginx-1.16.1/Makefile install

modules:
	$(MAKE) -f nginx-1.16.1/Makefile modules

upgrade:
	/usr/sbin/nginx -t

	kill -USR2 `cat /var/run/nginx.pid`
	sleep 1
	test -f /var/run/nginx.pid.oldbin

	kill -QUIT `cat /var/run/nginx.pid.oldbin`
