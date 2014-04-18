# lxc-1.0.3 rpm build tools (with python-3.4.0 bindings)

!!! USER AT YOUR OWN RISK !!!
It's not tested carefully

## BUILD:

````
yum install python34-python python34-python-devel -y
````

install build tools as lxc needed(gcc, etc... )


````
mkdir -p ~/rpmbuild/SOURCES/
cd ~/rpmbuild/SOURCES/
wget --no-check-certificate http://linuxcontainers.org/downloads/lxc-1.0.3.tar.gz
PYTHONDEV_CFLAGS=-I/usr/include/python3.4m PYTHONDEV_LIBS="-L/usr/lib -lpython3.4m"  PKG_CONFIG_PATH=/usr/lib/pkgconfig rpmbuild -bb lxc.spec


