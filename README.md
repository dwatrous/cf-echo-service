CloudFoundry Echo Service (to validate a Service Broker API)
===============

A basic echo service to validate a [Service Broker API v2.3 implementation](https://github.com/dwatrous/cf-service-broker-python) implementation for CloudFoundry, Stackato, or HP Helion Development Platform. This service was designed to respond to provision, bind, unbind and deprovision requests as defined by the [Service Broker API v2.3 specification](http://docs.cloudfoundry.org/services/api.html). This is relevant for CloudFoundry, Stackato and HP Helion Development Platform.

#### Dependencies
 * Python 3.x
 * bottle (http://bottlepy.org/docs/dev/index.html)

# Usage

The echo service can be run easily on any system that satisfies the dependiencies above. This repository also contains artifacts that make it easy to deploy to Stackato or HP Helion Development Platform.

## Windows
Clone this repository on to your Windows machine. Change into the directory where the files were cloned and use the python executable to run the script. The console session will look like the snippet below.

```
C:\Users\watrous\Documents\GitHub\cf-echo-service>\Python32\python.exe echo-service.py
Bottle v0.13-dev server starting up (using WSGIRefServer())...
Listening on http://0.0.0.0:8090/
Hit Ctrl-C to quit.
```

## Linux
Clone this repository on to your Linux system. Change into the directory and run the script. The session will look something like what's shown below.

```
vagrant@vagrant-ubuntu-trusty-64:~/cf-echo-service$ python3 echo-service.py
Bottle v0.12.7 server starting up (using WSGIRefServer())...
Listening on http://0.0.0.0:8090/
Hit Ctrl-C to quit.
```

## Deployed
Using the stackato or helion cli, the script can be deployed. The snippet below shows what that looks like.

```
C:\Users\watrous\Documents\GitHub\cf-echo-service>stackato push
Would you like to deploy from the current directory ?  [Yn]:
Using manifest file "manifest.yml"
Application Deployed URL [echo-service.stackato.danielwatrous.com]:
Application Url:   https://echo-service.stackato.danielwatrous.com
Creating Application [echo-service] as [https://api.stackato.danielwatrous.com -> Test -> somespace -> echo-service] ... OK
  Map https://echo-service.stackato.danielwatrous.com ... OK
Bind existing services to 'echo-service' ?  [yN]:
Create services to bind to 'echo-service' ?  [yN]:
Uploading Application [echo-service] ...
  Checking for bad links ...  OK
  Copying to temp space ...  OK
  Checking for available resources ...  OK
  Processing resources ... OK
  Packing application ... OK
  Uploading (3K) ...  OK
Push Status: OK
Starting Application [echo-service] ...
OK
http://echo-service.stackato.danielwatrous.com/ deployed
```
