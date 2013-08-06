Technicolor TG788vn router (OVH) telnet configuration scripts
=============================================================

Author: Gaëtan HARTER - hartergaetan@gmail.com

[External Documentation in French](http://cladmi.eu/dokuwiki/doku.php?id=informatique:configuration_modem_ovh_tg788vn_telnet)


I just wrote some scripts to configure the OVH router via telnet instead of using the web interface.
I publish them in case it might help someone.


Configuration
-------------

You should configure `router_ip`, `username` and `password` in the `wrapper_script.expect` file.

Some scripts requires you to configure them to fit your needs too. Please always read a script before running it.

Usage
-----

    ./wrapper_script.expect <script_to_run>


After some modifications, changes must be saved on the router to be available after reboot

    ./wrapper_script.expect save_all_config



How it works
------------


The scripts are based on `expect`.

They consist of a wrapper, which connects to the router and configure an alias which executes command and wait for the prompt.
Then execute the script given in parameter.

The executed scripts should be a sequence of `exec_cmd ":cmd to run on router"`.

