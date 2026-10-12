# Talkflow policy

`policy.json` is read by Talkflow 1.2 and later every few hours. `policy.json.sig` is its signature. It announces new versions and, in future, notices and plan rules. The app accepts it only if Zehnix's signature is valid; anything else is ignored.

It contains no information about anyone. Fetching it is a plain download.

To change it, edit `policy.json`, raise `issued` (UTC, ISO 8601), and sign it with the offline key:

```powershell
python tools\sign_policy.py ..\talkflow-releases\policy\policy.json
```

Run this in the Talkflow source checkout. Commit both files together.
