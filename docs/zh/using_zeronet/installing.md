# 安装ZeroNet

* 下载ZeroBundle包: [Microsoft Windows](https://github.com/HelloZeroNet/ZeroNet-win/archive/dist/ZeroNet-win.zip), [Apple macOS](https://github.com/HelloZeroNet/ZeroNet-mac/archive/dist/ZeroNet-mac.zip), [Linux 64bit](https://github.com/HelloZeroNet/ZeroBundle/raw/master/dist/ZeroBundle-linux64.tar.gz), [Linux 32bit](https://github.com/HelloZeroNet/ZeroBundle/raw/master/dist/ZeroBundle-linux32.tar.gz)
* 随地解压
* 运行 `ZeroNet.exe` (win), `ZeroNet(.app)` (macOS), `ZeroNet.sh` (linux)

### Debian Linux的手动安装

* `sudo apt-get update`
* `sudo apt-get install msgpack-python python-gevent`
* `wget https://github.com/HelloZeroNet/ZeroNet/archive/master.tar.gz`
* `tar xvpfz master.tar.gz`
* `cd ZeroNet-master`
* Start with `python zeronet.py`
* 在浏览器中打开 http://127.0.0.1:43110/

### [Vagrant](https://www.vagrantup.com/)

* `vagrant up`
* Access VM with `vagrant ssh`
* `cd /vagrant`
* 运行 `python zeronet.py --ui_ip 0.0.0.0`
* 在浏览器中打开 http://127.0.0.1:43110/

### [Docker](https://www.docker.com/)
* `docker run -d -v <local_data_folder>:/root/data -p 15441:15441 -p 127.0.0.1:43110:43110 nofish/zeronet`
* This Docker image includes the Tor proxy, which is disabled by default. Beware that some
hosting providers may not allow you running Tor in their servers. If you want to enable it,
set `ENABLE_TOR` environment variable to `true` (Default: `false`). E.g.:

 `docker run -d -e "ENABLE_TOR=true" -v <local_data_folder>:/root/data -p 15441:15441 -p 127.0.0.1:43110:43110 nofish/zeronet`
* 在浏览器中打开 http://127.0.0.1:43110/

### [Virtualenv](https://virtualenv.readthedocs.org/en/latest/)

* `virtualenv env`
* `source env/bin/activate`
* `pip install msgpack-python gevent`
* `python zeronet.py`
* 在浏览器中打开 http://127.0.0.1:43110/

