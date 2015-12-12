# go-github-how-to

##The GO language & Github how to for beginners

* The GO Project
Go is an open source project developed by a team at Google and many contributors from the open source community. 
Visit https://golang.org/project/ for documentation 

* GitHub 
A platform for hosting and collaborating on projects
Visit https://github.com for more details

## Pre-requisites

* OS - CentOS 7 
* A non-root user account in OS for development environment [ with your name ;-) ]
* Internet connection to download necessary rpm packages ( We will be using `yum` for installing packages )

### YUM configuration

* Create a diretcory called /DVD & mount CentOS 7 DVD over it
* Note down the Media ID** from /DVD/.discinfo file
* Create a file /etc/yum.repos.d/CentOS-DVD.repo and add below entries
```bash
[CentOS-7-DVD]
name=CentOS-$releasever - Base
baseurl=file:///DVD/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
enabled=1
mediaid=1427495138.035654 # **Media ID 
```

* Enable /etc/yum.repos.d/CentOS-Base.repo by updating parameter `enabled=1`

### Installation

* `yum install golang golang-vim`

### Environment Setup for GO

* Create a Github public account if you don't have 
* Add a new repository on Github ( Dropdown option will come after clicking topbar + sign )
* Create environemnt for GO by executing below
```bash
$ mkdir $HOME/work
$ export GOPATH=$HOME/work
$ cd $GOPATH
$ mkdir src pkg bin
$ cd src
$ mkdir -p github.com/ansilh/go-how-to
$ export PATH=$PATH:$GOPATH/bin
$ cd github.com/ansilh/go-how-to
```

### Hello World program

* `vi hello.go` # This program is there in source tree as hello/hello.go , you can download it
* `go install github.com/ansilh/go-how-to/hello`
* Now you will get a file in `$GOPATH/bin/` called `hello`
* Execute it `hello` will display below

`Hello, world.`

### Push your project to Github

```bash
$ cd GOPATH=$HOME/work/src/github.com/ansilh/go-how-to
$ git init
$ git add .
$ git commit -m "Initial commit"
$ git remote add origin https://github.com/ansilh/go-how-to.git
$ git remote -v
$ git push origin master
```

### Verify your project in Github
