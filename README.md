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
        memcached_properties:
          - {regexp: "^-p .*", line: "-p 1337"}
          - {regexp: "^-m .*", line: "-m 4096"}
          - {regexp: "^-c .*", line: "-c 2000"}
      }



see box-example folder of the repo for standalone deployment


Copyright and license
---------------------

Copyright - Vyacheslav Voronenko

Code licensed under the [BSD 3 clause] (https://opensource.org/licenses/BSD-3-Clause) or the [MIT License] (http://opensource.org/licenses/MIT).

Subscribe for roles updates at [FB] (https://www.facebook.com/SoftAsap/)

