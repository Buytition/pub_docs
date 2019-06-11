# Release Notes
## Upcoming Release
None
## 20190610
We are excited to announce the launch of replybot.io domain name as well as release of Reader Bot API v1.0.0 to the public.  Reader Bot API will be hosted under replybot.io domain name for ease of memorizing.  This API brings developers programmatic access to [Reader Bot](https://github.com/Buytition/pub_docs/blob/master/FEATURES.md#email-reader-bot) which has powered [Buytition web app](https://buytition.com) since its launch.  With this access, developers will be able to build your own

* Email apps that detects and extracts dealer and  vehicle price quotes info from raw email messages
* Vehicle price quote database

Along with this release,  version of the underlying reader bot has been upgraded to v1.0.0.  Below are specs for the API

* End point: `https://replybot.io/api/v1/readerbot`
* Accepted Method: post
* Input: text, html or URL
* Output: whether the input text has vehicle price quotes or not, if so list of vehicle price quotes, whether or not the input text has dealer info, if so the info of dealer, metadata of input
* Output format: json

Sample API call

Input
```
curl --data "URL=https://raw.githubusercontent.com\
/Buytition/pub_docs/master/raw-text/html-20190525-jerrysford.md" \
https://replybot.io/api/v1/readerbot
```

Output
```json
{
    "elapsed_sec": 0.9,
    "finish_utc": "2019-05-31 01:41:05",
    "input": {
        "URL": "https://raw.githubusercontent.com/Buytition/pub_docs/master/raw-text/html-20190525-jerrysford.md",
        "content-length": "46558",
        "content-type": "text/plain; charset=utf-8",
        "type": "EMAIL-TEXT",
        "via": "POSTED-URL"
    },
    "msg": null,
    "output": {
        "list_quotes": [
            {
                "MSRP": 45575,
                "make": "ford",
                "model": "edge",
                "quote_amt": 34296,
                "saving_amt": 11279,
                "saving_pct": 24.7,
                "year": 2019
            }
        ],
        "num_quotes": 1
    },
    "status": "success"
}
```