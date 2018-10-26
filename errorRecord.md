## 安装edgex-go时zeromq遇到的问题和解决方法

```
wget https://github.com/zeromq/libzmq/archive/v4.2.3.tar.gz
tar zxvf v4.2.3.tar.gz
cd libzmq-4.2.3/
./autogen.sh
./configure --prefix=/usr
make
make install
```
check:
```
$ ls /usr/lib/libzmq.*
/usr/lib/libzmq.a /usr/lib/libzmq.so /usr/lib/libzmq.so.5.1.3
/usr/lib/libzmq.la /usr/lib/libzmq.so.5
```
or the fastest way is download from repository:
```apt-get install libzmq3-dev```


# pkg-config --cflags  -- libzmq
Package libzmq was not found in the pkg-config search path.
Perhaps you should add the directory containing `libzmq.pc'
to the PKG_CONFIG_PATH environment variable
No package 'libzmq' found

```
export PKG_CONFIG_PATH=/usr/local/lib/pkgconfig
```
