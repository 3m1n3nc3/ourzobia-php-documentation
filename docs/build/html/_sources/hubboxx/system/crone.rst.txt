********************
Setting up Cron Jobs
********************

There are times when the system may be unable to acquire required and useful data from the client due to network down times and other unforeseen circumstances, when this happens, the system has been designed to process all available scraps and generate useful data at it's own convenience, this is made possible with the use of Cron Jobs.

To setup the system for this functionality, create a crone job at your server pointing to ``project_dir/public/index.php cli index``

 
Manage Cron Jobs
=================

After setting up crone jobs on your server your next step would be to turn them on.
Login to the admin dashboard and point your web browser to ``http://yourdomain.com/admin/configuration/system`` where ``yourdomain.com`` is your actual domain name or click on ``Management`` > ``Configuration`` > ``System`` on the admin dashboard.

*Cron Jobs management requires you to be looged in as an admin*.

Scroll down to **System** and Toggle on the ``Crone Jobs`` switch.

.. toctree::
    :glob:
    :titlesonly: