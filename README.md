App Dev Cloud with JBoss Cool Store Demo 
==========================================
This demo is to install JBoss Cool Store in the Cloud based on leveraging any Red Hat OpenShift container
based platform, such as 

 - [Red Hat Container Platform (OCP)](https://github.com/redhatdemocentral/ocp-install-demo)
  
 - [Red Hat Container Development Kit (CDK)](https://github.com/redhatdemocentral/cdk-install-demo)

It delivers a fully functioning containerized JBoss Cool Store.

The Cool Store is a retail web store demo where you will find rules, decision tables, events, and a ruleflow 
that is leveraged by a web application. The web application is a WAR built using the JBoss BRMS
generated project as a dependency, providing an example project showing how developers can focus on the 
application code while the business analysts can focus on rules, events, and ruleflows in the 
JBoss BRMS product web based dashboard.

This demo is self contained, it uses a custom maven settings to deploy all built JBoss BRMS knowledge artifacts
into an external maven repository (not your local repository), in /tmp/maven-repo.


Install JBoss Cool Store on OpenShift
-------------------------------------
1. First ensure you have an OpenShift container based installation, such as one of the followling installed first:

  - [OCP Install Demo](https://github.com/redhatdemocentral/ocp-install-demo)

  - [CDK Install Demo](https://github.com/redhatdemocentral/cdk-install-demo)

  - or your own OpenShift installation.

2. [Download and unzip this demo.](https://github.com/redhatdemocentral/rhcs-coolstore-demo/archive/master.zip)

3. Add products to installs directory.

4. Run 'init.sh' or 'init.bat' file. 'init.bat' must be run with Administrative privileges:
```
   # The installation needs to be pointed to a running version
   # of OpenShift, so pass an IP address such as:
   #
   $ ./init.sh 192.168.99.100  # example for OCP.

   $ ./init.sh 10.1.2.2        # example for CDK.
```

Login to Cool Store to start exploring a retail web shopping project (the address will be generated by the init script):

  - OCP example: [http://rhcs-coolstore-demo.192.168.99.100.xip.io/business-central](http://rhcs-coolstore-demo.192.168.99.100.xip.io/business-central)  ( u:erics / p:jbossbrms1! )

  - OCP example web app: [http://rhcs-coolstore-demo.192.168.99.100.xip.io/brms-coolstore-demo](http://rhcs-coolstore-demo.192.168.99.100.xip.io/brms-coolstore-demo)

  - CDK example: [http://rhcs-coolstore-demo.10.1.2.2.xip.io/business-central](http://rhcs-coolstore-demo.10.1.2.2.xip.io/business-central)  ( u:erics / p:jbossbrms1! )

  - CDK example web app: [http://rhcs-coolstore-demo.10.1.2.2.xip.io/brms-coolstore-demo](http://rhcs-coolstore-demo.10.1.2.2.xip.io/brms-coolstore-demo)


Note before running demo:
-------------------------
This project can be installed on any OpenShift platform, such as OpenShift Container Platform or Red Hat Container Development Kit.
It's possible to install it on any available installation by pointing this installer to an OpenShift IP address:
```
  $ ./init.sh IP
```

If for any reason the installation breaks or you want a new JBoss BRMS installation, just remove the project rhcs-brms-install-demo
entry in the OpenShift console and re-run the installation.

Should your local network DNS not handle the resolution of the above address, giving you page not found errors, you can apply the
following to your local hosts file:

```
$ sudo vi /etc/hosts

# add host for OCP demo resulution
192.168.99.100   rhcs-coolstore-demo.192.168.99.100.xip.io 

# add host for CDK demo resolution.
10.1.2.2   rhcs-coolstore-demo.10.1.2.2.xip.io 
```


Supporting Articles
-------------------
- [Ultimate Cloud Guide to Retail in the Cloud with JBoss Cool Store](http://www.schabell.org/2016/03/ultimate-cloud-guide-retail-cloud-jboss-coolstore.html)


Released versions
-----------------
See the tagged releases for the following versions of the product:

- v1.3 - JBoss BRMS 6.3.0 and JBoss EAP 6.4.7 with Cool Store installed on any given OpenShift installation.

- v1.2 - JBoss BRMS 6.3.0 and JBoss EAP 6.4.7 with Cool Store installed on Red Hat CDK.

- v1.1 - JBoss BRMS 6.2.0.GA-redhat-1-bz-1334704 and JBoss EAP 6.4.4 with Cool Store installed on Red Hat CDK.

- v1.0 - JBoss BRMS 6.2.0-BZ-1299002, JBoss EAP 6.4.4 with Cool Store installed on Red Hat CDK using OpenShift Enterprise image. 

![OSE pod](https://github.com/redhatdemocentral/rhcs-coolstore-demo/blob/master/docs/demo-images/rhcs-coolstore-pod.png?raw=true)

![OSE build](https://github.com/redhatdemocentral/rhcs-coolstore-demo/blob/master/docs/demo-images/rhcs-coolstore-build.png?raw=true)

![JBoss Store](https://github.com/redhatdemocentral/rhcs-coolstore-demo/blob/master/docs/demo-images/coolstore-shoppingcart-0.png?raw=true)

![JBoss BRMS](https://github.com/redhatdemocentral/rhcs-coolstore-demo/blob/master/docs/demo-images/jboss-brms.png?raw=true)

![Decision Table](https://github.com/redhatdemocentral/rhcs-coolstore-demo/blob/master/docs/demo-images/coolstore-decision-table.png?raw=true)

