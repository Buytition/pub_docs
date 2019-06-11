A run down of Buytition features

# Email Reader Bot
Buytition's proprietary Email Reader Robot (watch [demo video](https://www.youtube.com/watch?v=UZz7a5sni3A) to see the robot in action) utilizes text mining technology to parse car shopping email messages and automatically create vehicle price quote reports from them. Here is a list of robot capabilities (as of July 2017): 

* Edmunds PricePromise email, see sample [inbox message](https://github.com/Buytition/pub_docs/blob/master/raw-text/inbox-201812120906-edmunds-pricepromise.md) ([raw html](https://raw.githubusercontent.com/Buytition/pub_docs/master/raw-text/inbox-201812120906-edmunds-pricepromise.html)): extract dealer, vehicle, price quote and MSRP information automatically
* TrueCar Certified Dealer Quote emails: extract dealer, vehicle, price quote and MSRP information automatically
* Emails from non-Edmunds car shopping sites such as CarGurus.com: extract vehicle and price quote information automatically
* For eamils from any car dealers: extract dealer, vehicle, price quote and MSRP information automatically if they are available in the email message

All extracted dealer, vehicle, price quotes and MSRP information are displayed as a report to you in "My Quotes" section after you login.

Email Reader Robot is still at infancy stage, our goal is to give more and more strength to it overtime so that it will be able to do more and more sophisticated work of managing dealer emails traditionally done by car buyers manually. 

## Reader Bot API

This API brings developers programmatic access to [Reader Bot](https://github.com/Buytition/pub_docs/blob/master/FEATURES.md#email-reader-bot).  With this access, developers will be able to build your own

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
# Email Reply Bot

Buytition Email Reply Bot is an auto-response email solution for car buyers to automate replying car shopping related emails, it leverages vehicle quote information extracted by [Reader Robot](#email-reader-bot), automatically finds better price quote in Buytition vehicle quote database for same make and model and similar year vehicle and reply dealer email and request dealer to match the found better vehicle quote.

As of April 2019, Reply Bot responds to the following types of inbound emails
* Edmunds PricePromise Emails, example: for this [inbox message](https://github.com/Buytition/pub_docs/blob/master/raw-text/inbox-201812120906-edmunds-pricepromise.md) ([raw html](https://raw.githubusercontent.com/Buytition/pub_docs/master/raw-text/inbox-201812120906-edmunds-pricepromise.html)), Reply Bot will generate this [sent message](https://github.com/Buytition/pub_docs/blob/master/raw-text/sent-201812120906-edmunds-pricepromise.md) ([raw html](https://raw.githubusercontent.com/Buytition/pub_docs/master/raw-text/sent-201812120906-edmunds-pricepromise.md)).
