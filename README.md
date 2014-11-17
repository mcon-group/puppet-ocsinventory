# Puppet ocsinventory

## Build status

[![Build Status](https://travis-ci.org/arioch/puppet-ocsinventory.png?branch=master)](https://travis-ci.org/arioch/puppet-ocsinventory)


## Requirements

* [concat](https://github.com/ripienaar/puppet-concat)
* [stdlib](https://github.com/puppetlabs/puppetlabs-stdlib)

Debian only:

* Puppetlabs [apt module](https://github.com/puppetlabs/puppetlabs-apt) or
* Camptocamp [apt module](https://github.com/camptocamp/puppet-apt)


## Tested on...

* Debian 5 (Lenny)
* Debian 6 (Squeeze)
* CentOS 5
* CentOS 6


## Example usage

### Install ocsinventory

    node /box/ {
      include ocsinventory
    }

### Configure ocsinventory

    node /box/ {
      class { 'ocsinventory':
        pkg_ensure     => latest,
        service_ensure => running,
      }
    }

### Manage repository

    node /box/ {
      class { 'ocsinventory':
        manage_repo => true,
      }
    }


## Contributing

* Fork it
* Create a feature branch (`git checkout -b my-new-feature`)
* Run rspec tests (`bundle exec rake spec`)
* Commit your changes (`git commit -am 'Added some feature'`)
* Push to the branch (`git push origin my-new-feature`)
* Create new Pull Request

