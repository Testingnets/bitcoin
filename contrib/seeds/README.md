# Seeds

Utility to generate the seeds.txt list that is compiled into the client
(see [src/chainparamsseeds.h](/src/chainparamsseeds.h) and other utilities in [contrib/seeds](/contrib/seeds)).

Be sure to update `PATTERN_AGENT` in `makeseeds.py` to include the current version,
and remove old versions as necessary (at a minimum when GetDesirableServiceFlags
changes its default return value, as those are the services which seeds are added
to addrman with).

Place any ip addresses with port 8333 in nodes_main.txt, then run:

```
python3 generate-seeds.py . > ../../src/chainparamsseeds.h
```

Observe the hex values in chainparamsseeds.h
