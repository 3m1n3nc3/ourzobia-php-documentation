#####################
Setting up Crone Jobs
#####################

The automation of Ourzobia PHP is completely implemented with the CLI in order to ensure that users are only triggering processes that directly concerns them, while global activities affecting all users and the site as a whole are moved to the CLI and handled by Crone Jobs on the server side, this will ensure that load times are faster for the user.

There are typically two endpoints for Crone jobs in Ourzobia PHP:

1. ``ugrd_users`` endpoint handles system intensive tasks like:
    - Generating or Removing the default system user account
    - Upgrading users levels
    - Changing users guiders

    to setup the ``ugrd_users`` endpoint, create a crone job pointing to ``project_dir/public/index.php cli ugrd_users``

2. ``match_users`` endpoint handles system intensive tasks like:
    - Paying unpaid pledge referral bonuses
    - Reporting unpaid pledges to admin
    - Automatically matching cashout requests
    - Automatically matching donation requests

    to setup the ``ugrd_users`` endpoint, create a crone job pointing to ``project_dir/public/index.php cli match_users``


**********************
Manage Crone Jobs
**********************

After setting up crone jobs your next step would be to manage how these jobs are run.
To begin, login to the admin dashboard and point your web browser to ``http://yourdomain.com/admin/configuration/control`` where ``yourdomain.com`` is your actual domain name.

Cron Jobs
=========

Find the ``Cron Jobs`` settings, you have ``3 options`` to choose from. You can choose to disable crone jobs ``No`` or enable crone jobs ``Yes``. The system still has the ability to perform some basic crone tasks like pairing, but you can choose to turn that feature of by changing the setting to ``Only``

Auto Pair Pledges
=================

Find the ``Auto Pair Pledges`` settings, you have ``2 options`` to choose from. You can choose to disable pledge auto pairing ``No`` or enable pledge auto pairing ``Yes``.

Auto Pair Cashouts
==================

Find the ``Auto Pair Cashouts`` settings, you have ``2 options`` to choose from. You can choose to disable cashout auto pairing ``No`` or enable cashout auto pairing ``Yes``.