# ARMS Remote depot

Follow the instructions [here](https://pros.cs.purdue.edu/v5/cli/conductor.html?highlight=remote%20depot#creating-remote-depots) to add the ARMS remote depot key to your conductor.pros file. The following JSON object is what you want to add in the "depots" dict.

```
"arms-depot": {
                "config": {},
                "config-schema": {},
                "last_remote_update": {
                    "__reduce__": [
                        {
                            "py/type": "datetime.datetime"
                        },
                        [
                            "B+YEBxMwNwhM7Q=="
                        ]
                    ],
                    "py/object": "datetime.datetime"
                },
                "location": "https://mihirlaud.github.io/arms-depot/arms-depot.json",
                "name": "arms-depot",
                "py/object": "pros.conductor.depots.http_depot.HttpDepot",
                "remote_templates": [],
                "update_frequency": {
                    "py/reduce": [
                        {
                            "py/type": "datetime.timedelta"
                        },
                        {
                            "py/tuple": [
                                0,
                                60,
                                0
                            ]
                        }
                    ]
                }
            },
```

Then, run

```
pros c query --force-refresh
```

to download the latest ARMS release remotely.