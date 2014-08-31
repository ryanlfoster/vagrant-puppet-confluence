vagrant-puppet-confluence
===================

Vagrant example on installing confluence using puppet

Example
-------
```sh
$ git clone https://github.com/mkrakowitzer/vagrant-puppet-confluence.git
$ cd vagrant-puppet-confluence
$ sudo gem install librarian-puppet --verbose
$ librarian-puppet install
$ wget -O files/atlassian-confluence-6.3.4a.tar.gz \
  http://www.atlassian.com/software/stash/downloads/binary/atlassian-confluence-6.3.4a.tar.gz
```
Download jdk-7u65-linux-x64.tar.gz from here and copy into files directory:

http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html
 
```sh
vagrant up confluence1 (CentOS 6) (http://192.168.33.10)
vagrant up confluence2 (CentOS 5) (http://192.168.33.11)
vagrant up confluence3 (Ubuntu 12.04) (http://192.168.33.12)
```

License
-------
The MIT License (MIT)

Author
------------
* Merritt Krakowitzer merritt@krakowitzer.com
