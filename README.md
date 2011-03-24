## A little overlay for [unixODBC][unixodbc]

According [this][oracle] forum thread, with these addition unixODBC on 64bit linux will be able to connect oracle databases.

[unixodbc]: http://www.unixodbc.org/
[oracle]: http://forums.oracle.com/forums/thread.jspa?messageID=2427339

Copy paste how to:
    mkdir -p /usr/local/portage

    # clone the GIT repository
    git clone git://github.com/bonyiii/unixODBC.git /usr/local/portage

    # add the overlay to your make.conf
    cat >> /etc/make.conf <<\EOF
    PORTDIR_OVERLAY="${PORTDIR_OVERLAY} /usr/local/portage"
    EOF

    # install unixODBC
    emerge -av unixODBC

