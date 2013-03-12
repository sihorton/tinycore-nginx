tinycore-nginx
==============

Tinycore nginx extension (with 64-bit corepure64 version)

    http://wiki.nginx.org/Install#Building_Nginx_From_Source
    wget http://nginx.org/download/nginx-1.2.6.tar.gz
    tar xvzf nginx-1.2.6.tar.gz
    cd nginx-
    ./configure
    make

Original build.sh script downloaded from http://tinycorelinux.net/4.x/x86/tcz/src/nginx/build.sh
nginx.build64 is a modified version that has the correct flags for 64 bit compile.

submit script added to use tcztools to prepare output extension for submission
email.js script added to send email to tcesubmit email address using node & nodemailer.

Re-building
===========
Download the source code
Edit variables in nginx.build64 to contain new source code version
    ./nginx.build64
    ./submit nginx
    ./submit nginx-doc
    node email.js <from email address> <from email password> nginx
    node email.js <from email address> <from email password> nginx-doc

The last 2 steps will send out an email to the tcesubmit email address.

