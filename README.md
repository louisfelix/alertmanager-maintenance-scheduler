# alertmanager-maintenance-scheduler
A maintenance scheduler UI for Prometheus AlertManager

The project in its current status is meant to support a specific feature around the Alertmanager API, and that is to be able to schedule a finite number of repeating silences. The tool is intended to be used via its Web based UI.

### Building
To build simply run:
```bash
make build
```

### Configuration & Running
The tool relies on a YAML config file to specify the Alertmanager address it is supposed to send requests to:
```yaml
---
alertmanager_api: "http://localhost:9093/api/v2"
```

```bash
./alertmanager-maintenance-scheduler --config.file=/path/to/config.yml
```
