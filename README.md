# Drone cookbook
[![Build Status](https://travis-ci.org/justincampbell/chef-drone.png?branch=master)](https://travis-ci.org/justincampbell/chef-drone)

Installs [Drone](https://github.com/drone/drone), a CI server built on [Docker](https://www.docker.io).

# Requirements

## Chef

* Chef 11+

## Platforms

* Ubuntu 12.04
* Ubuntu 12.10
* Ubuntu 13.04
* Ubuntu 13.10 (Experimental)

# Usage

Include `recipe[drone]` in your run list.

# Attributes

These attributes are under the `node['drone']` namespace.

Attribute | Description | Type | Default
----------|-------------|------|--------
package_url | URL of the Drone package to download and install | String | [http://downloads.drone.io/latest/drone.deb](http://downloads.drone.io/latest/drone.deb)
temp_file | Path to store the downloaded package | String | /tmp/drone.deb
config_file | Location of Drone config file | String | /etc/init/drone.conf
droned_opts | Options to use when running Drone | String | --port=:80
# Recipes

* `recipe[drone]` Installs/Configures Drone
