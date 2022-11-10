# technical-assesment
Level 2 technical assesments

A.

I will explain to my Level 1 teammate that the most recommended way to schedule cache clearing is by setting up a server-side cron job.

Providing the PHP file rocket-clean-domain.php. This file should be uploaded in the WordPress root installation directory (this is also where the wp-config.php and wp-load.php are located). 

The customer can ask for help from their hosting provider on setting up the cron job to run the PHP file at a specified time. If we had information on what the name of their hosting provider is, it would be helpful, as we could just look for the knowledge-based article from that host and include that on the steps.


B.

The site and server access will help us a lot in troubleshooting what is really causing the issue.

This way, we can verify if it is really not clearing the cache. We will first run the PHP file (rocket-clean-domain.php) to see if it works and clears the cache; we will not yet check the cron job.

We can run it by simply accessing http://domain.com/rocket-clean-domain.php.

After running the PHP file, the cache folders /cache/domain.com and /cache/min should no longer exist, and we can proceed with checking the cron job.

If the cache folders still exist, then we can confirm that it really is not clearing.

We can check if it is caused by a plugin conflict by deactivating all the plugins and just keeping WP-Rocket active, then try to clear the cache again.

If not plugins, then it could be the theme.

We can also try to reinstall the WP-Rocket plugin and/or install a fresh WordPress core to rule out any corrupted files.

In setting up the cron job, we will check the PHP file path and schedule formatting if it is entered correctly. Furthermore, most hosting providers have a cron job manager, which is far easier to use than configuring cron job via SSH.
