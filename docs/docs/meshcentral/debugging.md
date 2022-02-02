Youtube video about  websockets: https://youtu.be/3vI4URd3VzU

`Trace=1` as a parameter in chrome dev tools for debugging


To log all database queries, change log_statement in /etc/postgresql/13/main/postgresql.conf

```
# CUSTOM
log_statement = 'all'           # none, ddl, mod, all
```

The stacktrace was logged to `stdout/journalctl`. Supposedly, you can enable debug logging for node modules by adding `DEBUG=<modulename>` to the environment. 

Adding this to `/etc/systemd/system/meshcentral.service` should do it but it didn't seem to do anything. 

I think that's because Mesh uses the trace logging in the browser instead of logging things in the server logs. 

```
Environment=DEBUG=mesh*
```

If you want to change node to meshcentral in journalctl, add this to /etc/systemd/system/meshcentral.service.
  
```
SyslogIdentifier=meshcentral
```
