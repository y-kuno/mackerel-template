# Example

Example dashboard & monitors template for mackerel.

## Required

```bash
mackerel-plugin-example
```

## Dashboard

### Creating Dashboard

```bash
$ curl -X POST -H "Content-Type:application/json"  -H "X-Api-Key:<Api-Key>" https://api.mackerelio.com/api/v0/dashboards -d @dashboard.json
```

### Screenshot

![Screenshot](docs/images/dashboard.png)

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
