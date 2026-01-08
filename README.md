# 40333

Reproduction for [Renovate issue 40333](https://github.com/renovatebot/renovate/issues/40333).

Renovate fails to read the EPEL repository with the following error:

```
DEBUG: Failed to fetch or decompress https://dl.fedoraproject.org/pub/epel/9/Everything/x86_64/repodata/61f7183e38b65817a31330a8a90f5c1ce700bfcd0ec96aad95251f243b3350cc-primary.xml.xz: incorrect header check
DEBUG: Datasource connection error
{
  "datasource": "rpm",
  "packageName": "python3.13-devel",
  "errCode": "Z_DATA_ERROR"
}
```

<details><summary>JSON logs</summary>

```json
{"name":"renovate","hostname":"jr-microvm","pid":694,"level":20,"logContext":"tRzkpc-sxOiBrSII106hf","repository":"rafsk-c365/renovate-python-epel-reprod","msg":"hostRules: no authentication for dl.fedoraproject.org","time":"2026-01-08T15:51:58.566Z","v":0}
{"name":"renovate","hostname":"jr-microvm","pid":694,"level":20,"logContext":"tRzkpc-sxOiBrSII106hf","repository":"rafsk-c365/renovate-python-epel-reprod","msg":"Using queue: host=dl.fedoraproject.org, concurrency=16","time":"2026-01-08T15:51:58.567Z","v":0}
{"name":"renovate","hostname":"jr-microvm","pid":694,"level":20,"logContext":"tRzkpc-sxOiBrSII106hf","repository":"rafsk-c365/renovate-python-epel-reprod","msg":"Failed to fetch or decompress https://dl.fedoraproject.org/pub/epel/9/Everything/x86_64/repodata/61f7183e38b65817a31330a8a90f5c1ce700bfcd0ec96aad95251f243b3350cc-primary.xml.xz: incorrect header check","time":"2026-01-08T15:51:59.749Z","v":0}
{"name":"renovate","hostname":"jr-microvm","pid":694,"level":20,"logContext":"tRzkpc-sxOiBrSII106hf","repository":"rafsk-c365/renovate-python-epel-reprod","datasource":"rpm","packageName":"python3.13-devel","errCode":"Z_DATA_ERROR","msg":"Datasource connection error","time":"2026-01-08T15:51:59.750Z","v":0}
{"name":"renovate","hostname":"jr-microvm","pid":694,"level":20,"logContext":"tRzkpc-sxOiBrSII106hf","repository":"rafsk-c365/renovate-python-epel-reprod","dependency":"python3.13-devel","packageFile":".python-version","msg":"Failed to look up rpm package python3.13-devel","time":"2026-01-08T15:51:59.751Z","v":0}
```
</details>
