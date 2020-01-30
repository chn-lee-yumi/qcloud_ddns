# qcloud_ddns

腾讯云域名DDNS的python2脚本，可以在群晖上使用

群晖使用方式：

```shell
root@CloudStation:~# cat /etc/crontab 
MAILTO=""
PATH=/sbin:/bin:/usr/sbin:/usr/bin:/usr/syno/sbin:/usr/syno/bin:/usr/local/sbin:/usr/local/bin
#minute	hour	mday	month	wday	who	command
0	0	1	*	*	root	/usr/syno/bin/syno_disk_health_record
0	0	3	*	*	root	/tmp/synoschedtask --run id=1
0	0	18	*/6	*	root	/tmp/synoschedtask --run id=3
8	1	11	2	*	root	/tmp/synoschedtask --run id=4
*/5   *   *   *   *   root    /bin/python /root/ddns.py >> /root/ddns.log
```
