## How to Install
. Place `power-manager` in `/bin`

. Make the program executable

```
sudo chmod +x /bin/power-manager
```

. Add this section to `rc.local`

```
# POWER MANAGER
if [ -x /bin/power-manager ]; then
    ( sleep 20; setsid nohup /bin/power-manager >> /var/log/power-manager 2>&1 ) &
fi
```

. Restart system
