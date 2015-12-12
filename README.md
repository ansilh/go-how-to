# go-how-to

The GO language how to for beginners

## Pre-requisites

* OS - CentOS 7 
* Internet connection to download necessary packages

### YUM configuration

* Create a diretcory called /DVD & mount CentOS 7 DVD over it
* Copy the media id from /DVD/.discinfo file
* Create a file /etc/yum.repos.d/CentOS-DVD.repo and add below entries

`[CentOS-7-DVD]`

`name=CentOS-$releasever - Base`

`baseurl=file:///DVD/`

`gpgcheck=1`

`gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7`

`enabled=1`

`mediaid=1427495138.035654`

* Enable /etc/yum.repos.d/CentOS-Base.repo by updating parameter `enabled=1`

### Installation
* `yum install golang golang-vim`

### Environment Setup for GO
* Create a Github public account if you don't have 
* `mkdir $HOME/work`
* `export GOPATH=$HOME/work`
* `cd $GOPATH`
* `mkdir src pkg bin`
* `cd  src`
* `mkdir -p github.com/ansilh/go-how-to`
* `export PATH=$PATH:$GOPATH/bin`
* `cd github.com/ansilh/go-how-to`
* `vi hello.go` # This program is there in source tree as hello/hello.go , you can download it
* `go install github.com/ansilh/go-how-to/hello`
* Now you will get a file in `$GOPATH/bin/` called `hello`
* Execute it `hello` will display below
`Hello, world.`

### Push your project to Github

* `cd GOPATH=$HOME/work/src/github.com/ansilh/go-how-to`
* `git init`
* `git add .`
* `git commit -m "Initial commit"`
* `git remote add origin https://github.com/ansilh/go-how-to.git`
* `git remote -v`
* `git push origin master`

### Verify your project in Github
