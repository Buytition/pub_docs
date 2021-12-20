[TOC]

This document is a run down of SaveNowClub and/or ReplyBot features.

# Email Reader Bot
SaveNowClub's proprietary Email Reader Robot (watch [demo video](https://www.youtube.com/watch?v=UZz7a5sni3A) to see the robot in action) utilizes text mining technology to parse car shopping email messages and automatically create vehicle price quote reports from them. Here is a list of robot capabilities (as of July 2017): 

* Edmunds PricePromise email, see sample [inbox message](https://github.com/Buytition/pub_docs/blob/master/raw-text/inbox-201812120906-edmunds-pricepromise.md) ([raw html](https://raw.githubusercontent.com/Buytition/pub_docs/master/raw-text/inbox-201812120906-edmunds-pricepromise.html)): extract dealer, vehicle, price quote and MSRP information automatically
* TrueCar Certified Dealer Quote emails: extract dealer, vehicle, price quote and MSRP information automatically
* Emails from non-Edmunds car shopping sites such as CarGurus.com: extract vehicle and price quote information automatically
* For eamils from any car dealers: extract dealer, vehicle, price quote and MSRP information automatically if they are available in the email message

All extracted dealer, vehicle, price quotes and MSRP information are displayed as a report to you in "My Quotes" section after you login.

Email Reader Robot is still at infancy stage, our goal is to give more and more strength to it overtime so that it will be able to do more and more sophisticated work of managing dealer emails traditionally done by car buyers manually. 

# Email Reply Bot

SaveNowClub's Email Reply Bot is an auto-response email solution for car buyers to automate replying car shopping related emails, it leverages vehicle quote information extracted by [Reader Robot](#email-reader-bot), automatically finds better price quote in SaveNowClub's vehicle quote database for same make and model and similar year vehicle and reply dealer email and request dealer to match the found better vehicle quote.

As of April 2019, Reply Bot responds to the following types of inbound emails
* Edmunds PricePromise Emails, example: for this [inbox message](https://github.com/Buytition/pub_docs/blob/master/raw-text/inbox-201812120906-edmunds-pricepromise.md) ([raw html](https://raw.githubusercontent.com/Buytition/pub_docs/master/raw-text/inbox-201812120906-edmunds-pricepromise.html)), Reply Bot will generate this [sent message](https://github.com/Buytition/pub_docs/blob/master/raw-text/sent-201812120906-edmunds-pricepromise.md) ([raw html](https://raw.githubusercontent.com/Buytition/pub_docs/master/raw-text/sent-201812120906-edmunds-pricepromise.md)).

# Reply Bot API
Reply Bot API is a collection of replybot.io API that offers entry points to Reader Bot and Reply Bot features in backend.

## API Access
Accessing Reply Bot and Reader Bot API requires a API key which is free to obtain. 

**Obtain an API Key**

* sign up to [savenowclub.com](https://savenowclub.com) web app for free.
* login to savenowclub.com web app, then visit [Settings](https://savenowclub.com/web/dist/settings_account) page, your API key will show up there, see screen shot below.

<img src="https://raw.githubusercontent.com/Buytition/pub_docs/master/images/screen-shot-buytition-setting-page.png" title="Your API key" style="max-width:100%">

**To Use API Key**, add `X-API-KEY`  header to your API request and supply your API key obtained from savenowclub.com web app.  See this curl command for example

```shell
curl --header "X-API-KEY: [API_KEY]" --data "URL=https://raw.githubusercontent.com\
/Buytition/pub_docs/master/raw-text/inbox-201812120906-edmunds-pricepromise.html" \
https://savenowclub.com/api/v1/reader_bot/get_vehicle_price_quotes
```

**Usage Plan**: your free obtained API keys automatically fall into **lite** usage plan with the following specs

* limit 1 request per second
* limit 5000 requests per month starting on 1st day of usage

To upgrade your usage plan, please contact buytition@gmail.com

## Reader Bot API

This API brings developers programmatic access to [Reader Bot](https://github.com/Buytition/pub_docs/blob/master/FEATURES.md#email-reader-bot).  To access this API, please read [API access](https://github.com/Buytition/pub_docs/blob/master/FEATURES.md#api-access) section.

Reader Bot API contains the following entry points:

* [vehicle price quotes reader API](#vehicle-price-quotes-reader-api), extracts vehicle and price quotes information, if any, from input text or html
* [vehicle dealer info reader API](#vehicle-dealer-info-reader-api), extracts vehicle dealer information, if any, from input text or html

### Unique Advantages

* While other entity extraction API vendors (such as [Lexalytics](https://www.lexalytics.com/technology/entity-extraction) or [ParallelDots](https://www.paralleldots.com/named-entity-recognition)) usually extract general entities (people, places, dates, companies, products, jobs, and titles), we are specialized in extracting vehicle and price quotes entities and their relationship from documents
* While other entity extraction API vendors usually process text form documents only, our API is capable to process both HTML and text form of documents

### Use Cases

* **Empower Your Chatbot NLU to Understand Pricing Intent** say you are developing a chatbot for a car dealer, integrating Reader Bot API into your chatbot's NLU will immediately give it the power of identifying pricing intent of customers.  The accuracy of pricing intent will be at level of vehicle year make and model and customer's desired price quotes.
* **Collect Competitive Vehicle Pricing Data Automatically**, say you have access to raw documents data with vehicle pricing either vehicle shopping email messages or a set of car dealer web pages, ,then you may use Reader Bot API to process these documents quickly and automatically build a vehicle and price quotes database, for example, the table below is a summary view from an automatically-built vehicle price quote database, the view shows number of quotes, minimum quote price and % off MSRP for all Ford models in a certain geographical area in a certain time frame.

|make	|model	|# of quotes	|min price $	|% off MSRP	|
|---	|---	|---	|---	|---	|
|ford	|escape	|18	|15899	|38	|
|ford	|focus	|13	|11900	|38	|
|ford	|f-150	|17	|18199	|36	|
|ford	|fusion hybrid	|1	|20497	|36	|
|ford	|fiesta	|11	|10420	|36	|
|ford	|fusion	|18	|14984	|33	|
|ford	|edge	|5	|20998	|27	|
|ford	|explorer	|17	|23999	|26	|
|ford	|mustang	|12	|19993	|24	|



* **Inbound Email Processing Automation**, for inbound email processing tool vendors, such as [Gmelius](https://gmelius.com) which offers smart follow-ups feature for sales workforce,  Reader Bot API empowers you to automatically identify car shopping emails, assign proper tags to them and extract dealer information and/or vehicle price quote information from them automatically.


### Vehicle Price Quotes Reader API

ReplyBot Vehicle Price Quotes Reader API is a service that automatically extracts vehicle model and price quotes from email or HTML documents. 

Use cases

* **Extract intents and entities for chatbots** Extract intents related to vehicle price quotes or negotiation as well as entities of vehicle price quotes from input text or html, produces the extracted entities in output json
* **Create smart search indexes** Extract structured data from email messages or web pages and create a smart index to allow you to search through millions of email messages quickly.
* **Build automated document processing workflow**: ReplyBot Vehicle Price Quotes Reader API can provide the inputs required to automatically process vehicle shopping related emails or web pages without human intervention.  For example, a webmail service provider can automate the generation of vehicle price quotes database using ReplyBot Vehicle Price Quotes Reader API. 

API Specs

* End point: `https://savenowclub.com/api/v1/reader_bot/get_vehicle_price_quotes`
* Authorization: API key, see [API access](#api-access) section
* Accepted Method: post
* Input: text, html or URL
* Output: whether the input text has vehicle price quotes or not, if so produce a list of vehicle price quotes, as well as metadata of input
* Output format: json

Sample API call

Input
```
curl --header "X-API-KEY: [API_KEY]" --data "URL=https://raw.githubusercontent.com\
/Buytition/pub_docs/master/raw-text/inbox-201812120906-edmunds-pricepromise.html" \
https://savenowclub.com/api/v1/reader_bot/get_vehicle_price_quotes
```
note: replace `[API_KEY]` with your own API key

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

ReplyBot Dealer Info Reader API is a service that automatically extracts vehicle dealer information from email or HTML documents.  This service automatically lookup email sender among merchant database using either sender email address or email content or both. If a match is found, this service returns the matched merchant information, as of now, the supported merchants are US vehicle dealers.

Use cases
 
* **Email sender lookup among a merchant database** Extract structured sender data from email messages and categorize emails by senders.
* **Automatically classify emails based on matched merchants**: ReplyBot Dealer Info Reader API can automatically identify emails sent from vehicle dealers in US and also automatically identifies exact dealer who send the email, this capability allows a webmail provider to automatically categorize emails sent from vehicle dealers from the rest of emails. 

API specs

* End point: `https://savenowclub.com/api/v1/reader_bot/get_dealer_info`
* Accepted Method: post
* Authorization: API key, see [API access](#api-access) section
* Input: text, html or URL
* Output: whether the input text has vehicle dealer information or not, if so produce list of vehicle dealers, as well as metadata of input
* Output format: json

Sample API call

Input
```
curl --header "X-API-KEY: [API_KEY]" --data "URL=https://raw.githubusercontent.com\
/Buytition/pub_docs/master/raw-text/inbox-201812120906-edmunds-pricepromise.html" \
https://savenowclub.com/api/v1/reader_bot/get_dealer_info
```
note: replace `[API_KEY]` with your own API key

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
