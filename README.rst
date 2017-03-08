
steps
--------
1, git clone 

::

  git clone https://git.openstack.org/openstack/refstack-client


2, setup env 

::

  ./setup_env -t 14.0.0

3, source venv
 
::

  source .venv/bin/activate

4, configure tempest.conf
   reference

::

   https://aptira.com/testing-openstack-tempest-part-1/
   https://github.com/hogepodge/defcore-tools


5, run tests

::

  ./refstack-client test -c tempest.conf -v --test-list "https://refstack.openstack.org/api/v1/guidelines/2016.08/tests?target=compute&type=required&alias=true&flag=false" 
