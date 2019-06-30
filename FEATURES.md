This document is a run down of Buytition and/or ReplyBot.io features.

# Email Reader Bot
Buytition's proprietary Email Reader Robot (watch [demo video](https://www.youtube.com/watch?v=UZz7a5sni3A) to see the robot in action) utilizes text mining technology to parse car shopping email messages and automatically create vehicle price quote reports from them. Here is a list of robot capabilities (as of July 2017): 

* Edmunds PricePromise email, see sample [inbox message](https://github.com/Buytition/pub_docs/blob/master/raw-text/inbox-201812120906-edmunds-pricepromise.md) ([raw html](https://raw.githubusercontent.com/Buytition/pub_docs/master/raw-text/inbox-201812120906-edmunds-pricepromise.html)): extract dealer, vehicle, price quote and MSRP information automatically
* TrueCar Certified Dealer Quote emails: extract dealer, vehicle, price quote and MSRP information automatically
* Emails from non-Edmunds car shopping sites such as CarGurus.com: extract vehicle and price quote information automatically
* For eamils from any car dealers: extract dealer, vehicle, price quote and MSRP information automatically if they are available in the email message

All extracted dealer, vehicle, price quotes and MSRP information are displayed as a report to you in "My Quotes" section after you login.

Email Reader Robot is still at infancy stage, our goal is to give more and more strength to it overtime so that it will be able to do more and more sophisticated work of managing dealer emails traditionally done by car buyers manually. 

# Email Reply Bot

Buytition Email Reply Bot is an auto-response email solution for car buyers to automate replying car shopping related emails, it leverages vehicle quote information extracted by [Reader Robot](#email-reader-bot), automatically finds better price quote in Buytition vehicle quote database for same make and model and similar year vehicle and reply dealer email and request dealer to match the found better vehicle quote.

As of April 2019, Reply Bot responds to the following types of inbound emails
* Edmunds PricePromise Emails, example: for this [inbox message](https://github.com/Buytition/pub_docs/blob/master/raw-text/inbox-201812120906-edmunds-pricepromise.md) ([raw html](https://raw.githubusercontent.com/Buytition/pub_docs/master/raw-text/inbox-201812120906-edmunds-pricepromise.html)), Reply Bot will generate this [sent message](https://github.com/Buytition/pub_docs/blob/master/raw-text/sent-201812120906-edmunds-pricepromise.md) ([raw html](https://raw.githubusercontent.com/Buytition/pub_docs/master/raw-text/sent-201812120906-edmunds-pricepromise.md)).

# Reply Bot API
Reply Bot API is a collection of replybot.io API that offers entry points to Reader Bot and Reply Bot features in backend.

## Reader Bot API

This API brings developers programmatic access to [Reader Bot](https://github.com/Buytition/pub_docs/blob/master/FEATURES.md#email-reader-bot).  With this access, developers will be able to build your own

* Email apps that detects and extracts dealer and  vehicle price quotes info from raw email messages
* Vehicle price quote database

The Reader Bot API has the following sub-API:
* [vehicle price quotes reader API](#vehicle-price-quotes-reader-api), extracts vehicle and price quotes information, if any, from input text or html
* [vehicle dealer info reader API](#vehicle-dealer-info-reader-api), extracts vehicle dealer information, if any, from input text or html

### Vehicle Price Quotes Reader API

ReplyBot Vehicle Price Quotes Reader API is a service that automatically extracts vehicle model and price quotes from email or HTML documents. 

Use cases
* **Create smart search indexes** Extract structured data from email messages or web pages and create a smart index to allow you to search through millions of email messages quickly.
* **Build automated document processing workflow**: ReplyBot Vehicle Price Quotes Reader API can provide the inputs required to automatically process vehicle shopping related emails or web pages without human intervention.  For example, a webmail service provider can automate the generation of vehicle price quotes database using ReplyBot Vehicle Price Quotes Reader API. 

API Specs
* End point: `https://api.replybot.io/v1/reader_bot/get_vehicle_price_quotes`
* Accepted Method: post
* Input: text, html or URL
* Output: whether the input text has vehicle price quotes or not, if so produce a list of vehicle price quotes, as well as metadata of input
* Output format: json

Sample API call

Input
```
curl --data "URL=https://raw.githubusercontent.com\
/Buytition/pub_docs/master/raw-text/inbox-201812120906-edmunds-pricepromise.html" \
https://api.replybot.io/v1/reader_bot/get_vehicle_price_quotes
```

Output
```json
{
    "elapsed_sec": 0.2,
    "finish_utc": "2019-06-16 20:41:03",
    "input": {
        "URL": "https://raw.githubusercontent.com/Buytition/pub_docs/master/raw-text/inbox-201812120906-edmunds-pricepromise.html",
        "content-length": "3750",
        "content-type": "text/plain; charset=utf-8",
        "type": "EMAIL-TEXT",
        "via": "POSTED-URL"
    },
    "msg": null,
    "output": {
        "list_quotes": [
            {
                "MSRP": 39990,
                "make": "ford",
                "model": "edge",
                "quote_amt": 35767,
                "saving_amt": 4223,
                "saving_pct": 10.6,
                "year": 2019
            }
        ],
        "num_quotes": 1
    },
    "status": "success"
}
```

### Vehicle Dealer Info Reader API

ReplyBot Dealer Info Reader API is a service that automatically extracts vehicle dealer information from email or HTML documents.  

Use cases
 
* **Automatically identify email senders** Extract structured sender data from email messages and categorize emails by senders.
* **Automatically classify emails based on senders**: ReplyBot Dealer Info Reader API can automatically identify emails sent from vehicle dealers in US and also automatically identifies exact dealer who send the email, this capability allows a webmail provider to automatically categorize emails sent from vehicle dealers from the rest of emails. 

API specs

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