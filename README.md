# nominatim-docker

- hammermc/nominatim-docker:latest dev
- hammermc/nominatim-docker:release-3.2.0 release-v3.2.0

It works as a standalone nominatim docker container .
All enviroments tune from dot.env file

After compose file you need to create database manually
 
To keep nominatim updated, start the nominatim-updatedb container every 24 hours.

REINITDB=1 - init you database if DB not exist,be careful with this 
options after restart docker it's recreate your DB.
Recommend use only in initial running.

REDOWNLOAD=0 - download data for import.

Sometimes create DB does not work correctly,
after all containers is up  you need to change WFS_SLEEP in bigger value
AND then redeployHard or try only redeployHard - it's sometimes work correctly.
