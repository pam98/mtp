
**Before You Begin**: Do not use OVH or IPHoster datacenters for MTProto.
### Install
On your server run
```bash
curl -o MTProtoProxyInstall.sh -L https://git.io/Jvlyt && bash MTProtoProxyInstall.sh
```
Wait until the setup finishes, you should be given the links. (using `systemctl status mtprotoproxy -l` will display said links as well)

To update, uninstall, change port, revoke secret or... the proxy, run this script again.
#### Managing The Proxy
##### Service
Use `systemctl start mtprotoproxy` to start, `systemctl stop mtprotoproxy` to stop and `systemctl status mtprotoproxy -l` to see logs of script.
##### Config
To manually config, proxy edit config.py in /opt/mtprotoproxy to change the config; Then restart the server using `systemctl restart mtprotoproxy` or just run script again.
##### Quota Limiter
Python version of the proxy has the ability to limit the users by the traffic they use. You can change the quota by re-running the script after the installation. But remember that if you restart the proxy, all of the usages will reset. (They start counting from 0 again.)
