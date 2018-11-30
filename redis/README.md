# redis

redis dashboard & monitors template for mackerel.

## Required

```bash
mackerel-plugin-redis
mackerel-plugin-multicore
```

## Dashboard

update variable `<service>:<role>`  
ex. `redis:redis`

### Creating Dashboard

You can obtain the API key from the API tab on [your organization's page](https://mackerel.io/my?tab=apikeys).

```bash
$ curl -X POST -H "Content-Type:application/json"  -H "X-Api-Key:<Api-Key>" https://api.mackerelio.com/api/v0/dashboards -d @dashboard.json
```

### Screenshot

![Screenshot](./docs/images/dashboard.png)

## Monitors

The monitors use mkr command.

### SetUp

To use mkr, first we will assign the API key to the environment variable.

```bash
$ export MACKEREL_APIKEY=<API key>
```

### Register monitor configurations

```bash
$ mkr monitors push -F monitors.json
```

### Screenshot

![Screenshot](./docs/images/monitors.png)
