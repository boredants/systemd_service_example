# systemd_service_example
Example systemd service file

Just a quick example of a systemd service file for a ruby application that I was having some trouble with...


[Unit]
Description=<DESCRIPTION>

[Service]
Type=forking
User=<USER>
Group=<GROUP>
WorkingDirectory=<PATH/TO/FILES>
ExecStart=/bin/bash -lc 'foreman start internalweb &'
ExecStop=/bin/bash -lc 'pkill foreman'

[Install]
WantedBy=multi-user.target
