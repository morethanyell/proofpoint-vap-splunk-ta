## Overview
In contrast to Proofpoint TAP Modular Input (https://splunkbase.splunk.com/app/3681/), this TA uses the Proofpoint People API to ingest VAP. These are JSON logs that aren't time-bound and are useful only as lookup. Because of that, the logs' value for _time is the same as _indextime.

It's important to perform dedup to keep your lookups updated.

## Notes

- To enable ingesting, user must have a Principal and Secret
- The source type to which the logs are assigned is pps:tap:vap
- The strucure of logs is JSON
- Logs are not time bound. hence it is not sensible to search the logs with specific time range in the intention of getting the "Very Attack People" in that time range

## Full disclosure / disclaimer:

This app was built using Splunk Add-on Builder. The author has no intention of making profit out of this. The app was built during the time the author is associated/employed (as of this writing, I still am) with Verizon Enterprise Solutions. The app is not built by ProofPoint nor by Verizon Enterprise Solutions. Any bugs or errors that may be found in this Splunk TA should be communicated to the author (daniel.l.astillero@gmail.com) and not to ProofPoint nor Verizon.