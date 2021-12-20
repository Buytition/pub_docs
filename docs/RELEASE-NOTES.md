# Release Notes

For latest release notes from SaveNowClub, please check out [SaveNowClub Blog](http://blog.savenowclub.com/)

## 20191011
Reader Bot API v1.1.0 Released

After 3 months of busy work, we are happy to announce the release of [Reader Bot API](https://github.com/Buytition/pub_docs/blob/master/FEATURES.md#reader-bot-api) v1.1.0.  The major enhancements are accuracy of extracted data of vehicle information and price quotes.  The following are some of major improvements we made to Reader Bot API recently:
* expand price entity ranges: expand price ranges
* expand vehicle entity ranges: pick up missing vehicle models
* overhaul decision and matching logic to solve vehicle and price quotes mismatch issue
improve accuracy of price entity labeling logic

If you have any thoughts or questions, please reach out to us at buytition@gmail.com

## 20190616
We are excited to announce the launch of a [Vehicle Dealer Info Reader API](https://github.com/Buytition/pub_docs/blob/master/FEATURES.md#vehicle-dealer-info-reader-api), a new sub-API of [Reader Bot API](https://github.com/Buytition/pub_docs/blob/master/FEATURES.md#reader-bot-api).  This sub-API extracts vehicle dealer information, if any, from a given input text or html data, below are specs for this API

* End point: `https://api.replybot.io/v1/reader_bot/get_dealer_info`
* Accepted Method: post
* Input: text, html or URL
* Output: whether the input text has vehicle dealer information or not, if so produce list of vehicle dealers, as well as metadata of input
* Output format: json

Sample API call

Input
```
curl --data "URL=https://raw.githubusercontent.com\
/Buytition/pub_docs/master/raw-text/inbox-201812120906-edmunds-pricepromise.html" \
https://api.replybot.io/v1/reader_bot/get_dealer_info
```

Output
```json
{
    "elapsed_sec": 0.1,
    "finish_utc": "2019-06-16 20:37:50",
    "input": {
        "URL": "https://raw.githubusercontent.com/Buytition/pub_docs/master/raw-text/inbox-201812120906-edmunds-pricepromise.html",
        "content-length": "3750",
        "content-type": "text/plain; charset=utf-8",
        "type": "EMAIL-TEXT",
        "via": "POSTED-URL"
    },
    "msg": null,
    "output": {
        "list_dealers": [
            {
                "dlr_addr": "1051 E Broad St, Falls Church VA 22044",
                "dlr_name": "Koons Ford of Falls Church",
                "id": 7821
            }
        ],
        "num_dealers": 1
    },
    "status": "success"
}
```

## 20190610
We are excited to announce the launch of replybot.io domain name as well as release of [Reader Bot API](https://github.com/Buytition/pub_docs/blob/master/FEATURES.md#reader-bot-api) v1.0.0 to the public.  Reader Bot API will be hosted under [replybot.io](https://api.replybot.io) domain name for ease of memorizing.  This API brings developers programmatic access to [Reader Bot](https://github.com/Buytition/pub_docs/blob/master/FEATURES.md#email-reader-bot) which has powered [Buytition web app](https://buytition.com) since its launch.  Along with this release,  version of the underlying reader bot has been upgraded to v1.0.0. With this access, developers will be able to build your own

* Email apps that detects and extracts dealer and  vehicle price quotes info from raw email messages
* Vehicle price quote database

Reader Bot API actually is a collection of sub-API entry points, each sub-API accomplishes one reader bot capability.  For this first release of Reader Bot API, we are releasing the [Vehicle Price Quotes Reader API](https://github.com/Buytition/pub_docs/blob/master/FEATURES.md#vehicle-price-quotes-reader-api) which extracts vehicle and price quotes information, if any, from a piece of given input text or html data. below are specs for this API

* End point: `https://api.replybot.io/v1/reader_bot/get_vehicle_price_quotes`
* Accepted Method: post
* Input: text, html or URL
* Output: whether the input text has vehicle price quotes or not, if so list of vehicle price quotes, whether or not the input text has dealer info, if so the info of dealer, metadata of input
* Output format: json

Sample API call

Input
```
curl --data "URL=https://raw.githubusercontent.com\
/Buytition/pub_docs/master/raw-text/html-20190525-jerrysford.md" \
https://api.replybot.io/v1/reader_bot/get_vehicle_price_quotes
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