leofs_package
=============

leofs_rpm is the leofs's configuration file for RPM(RedHat)/deb(Ubuntu)

###How to make RPM file

1. Prepare environment  
  * Install Git, rpmbuild, erlang  

2. Make working directories  
```bash
$ mkdir -p ~/rpm/{BUILD,RPMS,SOURCES,SPECS,SRPMS}
```

3. Copy spec file to 'SPECS' directory  
```bash
$ cp rpm/make_rpm.sh ~/rpm/SPECS  
$ cp rpm/leofs.spec ~/rpm/SPECS
```

4. Build RPM file  
```bash
$ cd ~/rpm/SPECS  
$ sh make_rpm.sh VERSION 
Example:  
$ sh make_rpm.sh 0.14.0  
``` 
  * RPM file is created in the 'RPMS' directory.

##How to make deb file

1. Prepare environment
  * Install Git, fakeroot, build-essential

2. Make working directories
```bash
$ mkdir {WORK_DIRECTORY}
 ```

3. Copy script file  
```bash
$ cp deb/make_deb.sh {WORK_DIRECTORY}
```

4. Build deb file
```bash
$ cd {WORK_DIRECTORY}
$ sh make_deb.sh {LeoFS's Version}
```
