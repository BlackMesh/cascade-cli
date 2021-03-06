CLI for Cascade that manages settings, services, and tasks.
 
# Build & Install
The only supported platform at the moment is CentOS 6 and the install must be done as root. Requires setuptools >= 1.1.6.
```
# yum install -y epel-release; yum clean all; yum install -y python-pip rpm-build
# pip install --upgrade setuptools
```
 
From source to RPM:
```
# python setup.py bdist_rpm
# rpm -i dist/cascade-cli-1.0.noarch.rpm
```

To uninstall:
```
# rpm -e cascade_cli-1.0.noarch
```

# Configuration
Any configurable settings should be found in: /etc/cascade-cli/config.ini

# Usage
Cascade-CLI operates in a server/client setup. One cannot function without the other.

To run as server, simply enter:
```
# cascade-cli --server
```

If the config.ini has a proper hosts entry, the client will connect simply via:
```
# cascade-cli
```

To view available commands:
```
# cascade-cli --help
```

# Authors
Developed by BlackMesh, Inc.  
Adam Schroeter (aschroeter@blackmesh.com)  
Solomon S Gifford (sgifford@blackmesh.com)
