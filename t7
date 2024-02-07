#!/bin/bash
DISK_USAGE=`df -kh | tail -2 | head -1 | awk -F " " '{print$5}' | sed 's/%//g'`
if [ $DISK_USAGE -gt 70 ]
then
  echo " take action & delete some files ....."
  sudo rm -f /tmp/*
  sudo rm -rf /opt/logs/*
  #mail -s "disk utilasation has gone beyond 70%" ajey@xyz.com teamlead@xyz.com
else
  echo "since disk usage is less than 70 , we are good...."
fi
