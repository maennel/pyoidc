Setup and run simple OP.
========================

Prerequisites for OP2:
**********************

* pysaml2 (available via the PyPi package repository)

* xmlsec1 (available via your OS package manager)

Setup OP2:
**********

The folder [your path]/pyoidc/oidc_example/op2 contains a file named oc_config.py.example

#. Take the file named **config.py.example** and copy it to a new file named **config.py**

#. Edit the file **config.py** and update the baseurl to the IP address of you local machine

#. Do the same with the file named **sp_conf.py.example**, copy it to **sp_conf.py** (it is referenced by the
   unchanged ``config.py``)

#. Prepare account metadata for the Identity Provider (IdP)
   by running ``make_metadata.py sp_conf > ./sp.xml`` inside the ``op2`` directory

Run OP2:
********

Open a Terminal::

    cd [your path]/pyoidc/oidc_example/op2
    python server.py -p 8092 -d config

Note that you should not have the .py extension on the config.py while running the program