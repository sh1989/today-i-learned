# List All Splunk Indices

In large Splunk instances, there are often many indices and discovering these is quite tricky. To list every index, run:
```
eventcount summarize=false index=* | dedup index | fields index
```
