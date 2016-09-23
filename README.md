sa-memcached
============

[![Build Status](https://travis-ci.org/softasap/sa-memcached.svg?branch=master)](https://travis-ci.org/softasap/sa-memcached)

memcached_properties: list of regexes in form (regexp, line) to adjust /etc/memcached.conf with necessary changes



Example of usage (all parameters are optional)

Simple

  roles:
    - {
        role: "sa-memcached"
      }


Advanced:


  roles:
    - {
        role: "sa-memcached",
        beanstalkd_properties:
          - {regexp: "^-p .*", line: "-p 1337"}
          - {regexp: "^-m .*", line: "-p 4096"}
          - {regexp: "^-c .*", line: "-p 2000"}
      }



