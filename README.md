## How to Install
. Place `system-tuner` in `/bin`

. Make the program executable

```
sudo chmod +x /bin/system-tuner
```

. Add this section to `rc.local`

```
# POWER MANAGER
if [ -x /bin/system-tuner ]; then
    ( sleep 20; setsid nohup /bin/system-tuner >> /var/log/system-tuner 2>&1 ) &
fi
```

. Restart system
