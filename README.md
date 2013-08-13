solr daemon for Apache Solr
======================================================
This script is very handy for keeping your Java-based Solr server running, 
even if your server has to reboot. Since it exists as a service on the
server, you can stop, start or restart it simply by:

  > service solr stop
  > service solr start
  > service solr restart


BEFORE INSTALLING:
======================================================
You will need to download and install Apache Solr. 
See http://lucene.apache.org/solr/ 

Then download this file and check the "start" section to ensure your 
paths match your installation. 


TO INSTALL:
======================================================

For RedHat Linux, copy the 'solr' file into your init.d directory at
  /etc/init.d/solr

Then set the privileges:
  > sudo chmod 755 /etc/init.d/solr

Next setup your symbolic links.
  > sudo ln -s /etc/init.d/solr /etc/rc3.d/S99solr
  > sudo ln -s /etc/init.d/solr /etc/rc5.d/S99solr
  > sudo ln -s /etc/init.d/solr /etc/rc3.d/K01solr
  > sudo ln -s /etc/init.d/solr /etc/rc5.d/K01solr

Finally, start the service. 
  > sudo service solr start
