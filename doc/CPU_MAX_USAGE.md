# Maximum CPU usage

Please read this document carefully, `max-threads-hint` (was known as `max-cpu-usage`) option is most confusing option in the miner with many myth and legends.
This option is just hint for automatic configuration and can't precise define CPU usage.

### Option definition
#### Config file:
```json
{
    ...
    "cpu": {
        "max-threads-hint": 80,
        ...
    },
    ...
}
```

#### Command line
`--cpu-max-threads-hint 80`

### Known issues and usage

* This option has no effect if miner already generated CPU configuration, to prevent config generation use `"autosave":false,`.
* Only threads count can be changed, for 2 core CPU only 2 values possible 50% and 80%, for 4 cores: 25%, 50%, 75%, 80%. etc. 
* You CPU may limited by other factors, eg cache.
