# PM2 Cheatsheet

> [!IMPORTANT]  
> The following commands are supported only on Linux and macOS platforms,
> Windows support is out of scope.

### Create/start a process
```
$ pm2 start <app_script> --name "<app_name>"
```

### Restart a process
```
$ pm2 restart <app_name_or_app_id>
```


### Restart with new/update environment variable(s)
```
$ pm2 restart <app_name_or_app_id> --update-env
```

### Stop a process
```
$ pm2 stop <app_name_or_app_id>
```

### Remove a process
```
$ pm2 delete <app_name_or_app_id>
```

### Save current state
```
$ pm2 save
```

### List all processes
```
$ pm2 list
```

### View logs
```
$ pm2 logs <app_name_or_app_id>
```

### Show environment variables
```
$ pm2 env <app_name_or_app_id>
```

## Example  
run.sh script — change the shebang to the correct shell (use Bash in this case)  
```
#!/bin/bash

source .env
pm2 start dist/server.js --name "demo_svc"

```

