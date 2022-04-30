
# Welcome to abcdesktop.io, a desktopless system

abcdesktop.io = NoVNC + X11 + Docker

abcdesktop.io is a cloud native desktopless system, and a complete work environment accessible from a simple HTML 5 web browser, without any installation. Like serverless does, desktopless computing allocates desktop resources on demand.  **Each user’s application runs as a container** to reduce attack surface.
abcdeskop.io is an opensource and free solution that offer seamless access to secure desktops and applications on any device, follow the [https://github.com/abcdesktopio](https://github.com/abcdesktopio) links.

## Quick online preview
You can discover abcdesktop.io desktopless services on the demo website. [https://demo.abcdesktop.io](https://demo.abcdesktop.io) instance is a quick example to illustrate how the abcdesktop.io project works. Your desktopless is ready to run for 10 minutes, and will be terminated by the garbage collector after 10 minutes. It requires an OpenID Connect provider to sign-in like (Google, Facebook, Github). The security policy for Internet network prevents requests from your abcdesktop being allowed.
External network access is denied. Printer service (using cups) and sound service (using pulseaudio) inside the kubernetes pods are enabled.

* To reach the demo website, follow the link [https://demo.abcdesktop.io](https://demo.abcdesktop.io)
* To read more about abcdesktop.op, follow the link [https://www.abcdesktop.io](https://www.abcdesktop.io)


## abcdesktop.io: a docker VDI service

abcdesktop.io provides a way to run grapicals applications securely isolated in a docker container, and use a web browser HTML5 as display device. Because docker containers are lightweight and run without the extra load of an operating system, you can run many graphical applications on a single kernel or even on a kubernetes cluster.

![screenshot-applications](img/screenshot-applications.png)

## Quick installation for kubernetes

Download and extract the latest release automatically (Linux or macOS) or read the step by step installation process [abcdesktop for kubernetes](/setup/kubernetes_abcdesktop/)

```
curl -sL https://raw.githubusercontent.com/abcdesktopio/conf/main/kubernetes/install.sh | sh -
```

## Quick installation for docker (personal use, Non-cluster mode)

Download and extract the latest release automatically (Linux or macOS) or read the step by step installation process [abcdesktop for docker](/setup/dockermode/)

```
curl -L https://raw.githubusercontent.com/abcdesktopio/conf/main/docker/install.sh | sh -
```

## Features

- Complete native cloud desktop, workspace environment
- Authentification OAuth 2.0, LDAP, LDAPS, Active Directory, Kerberos
- Access to the user home directory (homeDirectory support in Active Directory)
- Legacy CIFS Flexvolume using kubernetes driver 
- All applications run inside an isolated docker container
- Local and remote printing support 
- Off-line sessions are maintained
- No need to install applications any more
- Application update, run latest docker image
- Accounting and reporting 
- Clipboard syncing
- Sound support with webrtc gateway and RTP stream

### Applications

- Native support GNU/Linux console native support
- Native support GNU/Linux X11 applications native support
- Support Microsoft Windows applications using wine

### Supported web browser HTML

abcdesktop.io uses many modern web technologies. However these are the minimum versions we are currently aware of:

* Chrome 49, 
* Firefox 58, 
* Safari 11, 
* Opera 36,  
* Microsoft Edge (based on Chromium)

#### copy and paste features
To fully use `copy and paste` features, from your local device to your abcdesktop (and vice versa), choose `Chrome`, Chromium or  Microsoft Edge Chromium. The `copy and paste` feature is also supported on Firefox with a [dedicated abcdesktop extension](/common/firefox-extension).

| Web browser      | Clipboard sync                 |
|------------------|-------------------------------------|
|  Chrome     | Yes, built in support |
|  Chromium     | Yes, built in support  |
|  Microsoft Edge Chromium     | Yes, built in support  |
|  Firefox       | Yes, install the [dedicated abcdesktop extension](/common/firefox-extension)| 
|  Safari       | No, the clipboard access is not allowed by the user agent or the platform in the current context, possibly because the user denied permission| 

### Not supported web browser

abcdesktop.io does NOT support Microsoft Internet Explorer from version 1.x to 11.x. If you need a Microsoft web browser use Microsoft Edge. Edge is based on the Chromium open-source project. Chromium forms the basis of Google Chrome, so the new Edge feels very similar to Google Chrome.

## Github repositories ![Github stars](https://img.shields.io/github/stars/abcdesktopio?style=social)

abcdesktop has 36 repositories available. Follow the code on GitHub [https://github.com/abcdesktopio](https://github.com/abcdesktopio) to get the source code.
