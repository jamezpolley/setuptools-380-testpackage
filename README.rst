setuptools #380 test package
============================

https://bitbucket.org/pypa/setuptools/issue/380/environment-markers-dont-support-etc

To reproduce, run these steps inside a checkout of this repo.

 - virtualenv .
 - source bin/activate
 - python setup.py egg_info - no problem; env-marked requirements are listed in .egg-info/requires.txt
 - pip install . - no error, but env-marked reqs are not installed
 - pip install pbr
 - python setup.py egg_info - "invalid environment marker" error.
 - pip install . - same
