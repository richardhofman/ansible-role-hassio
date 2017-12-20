richardhofman.hassio
=========

This Ansible role installs Hass.io on a Docker host - including Raspberry Pi. Support is implemented
for Ubuntu and CentOS 7.x, but only currently tested on CentOS. Eventually I intend to add support for
the same series of machines as the [Hass.io installation script](https://raw.githubusercontent.com/home-assistant/hassio-build/master/install/hassio_install), which this is based off.

Requirements
------------

The target host must have Docker installed and the Docker Engine running and functional before this playbook is deployed to it. The playbook *should* install all other requirements.

Role Variables
--------------

The role exposes a variety of configuration variables, most of which are likely to be fine left as default.

    machine: qemux86-64 # see: https://github.com/home-assistant/hassio-build/tree/master/install#install-hassio
    docker_repo: homeassistant
    data_dir: /usr/share/hassio
    bin_dir: /usr/bin
    version_url: https://raw.githubusercontent.com/home-assistant/hassio/master/version.json
    start_hassio_url: https://raw.githubusercontent.com/home-assistant/hassio-build/master/install/misc/hassio-start
    supervisor_service_url: https://raw.githubusercontent.com/home-assistant/hassio-build/master/install/systemd/hassio-supervisor.service
    hostcontrol_service_url: https://raw.githubusercontent.com/home-assistant/hassio-build/master/install/systemd/hassio-hc.service
    hostcontrol_generic_url: https://raw.githubusercontent.com/home-assistant/hassio-build/master/install/hassio_install

Dependencies
------------

N/A

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: hass
      roles:
         - { role: richardhofman.hassio, machine: qemux86-64 }

License
-------

MIT

Author Information
------------------

I am a software developer and devops engineer/site reliability engineer in Auckland, New Zealand. Just starting out in my career and still love my work enough to continue using the same technologies in my free time.

(c) Richard Hofman, 2017.