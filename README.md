Technicolor TG788vn router (OVH) telnet configuration scripts
=============================================================

Author: Gaëtan HARTER - hartergaetan@gmail.com


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


