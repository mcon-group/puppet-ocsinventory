# Puppet OCSInventory

## Build status

# [![Build Status](https://travis-ci.org/arioch/puppet-ocsinventory.png?branch=master)](https://travis-ci.org/arioch/puppet-ocsinventory)


## Requirements

* OCSInventory packages:
  can be obtained from ICS directly.
  https://www.ocsinventory-ng.org/en/rpm-repository-is-available-for-rhelcentosfedora/
* MySQL and apache are not managed by this module


## Tested on...

* CentOS 7
* Scientific Linux 6

## Example usage

### Install OCSInventory

    node /box/ {
      include ocsinventory
    }

### Configure OCSInventory

    node /box/ {
      class { 'ocsinventory':
        agent_ocs_mode   => 'cron',
        agent_ocs_pause  => '100',
        agent_ocs_server => 'localhost',
        agent_ocs_tag    => undef,
      }
    }

### Configure OCSInventory server

    node /box/ {
      class { 'ocsinventory':
        agent  => true, # default
        server => true,
      }
    }

## Contributing

* Fork it
* Create a feature branch (`git checkout -b my-new-feature`)
* Run rspec tests (`bundle exec rake spec`)
* Commit your changes (`git commit -am 'Added some feature'`)
* Push to the branch (`git push origin my-new-feature`)
* Create new Pull Request
