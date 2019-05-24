# Release Notes
## Upcoming Release

We are excited to announce the release of reader bot API v1.0.0 to the public.  This API brings developers programmatic access to buytition reader bot which has been powering buytition web app for two years.  With this access, developers will be able to build your own

* Email apps that detects and extracts dealer and  vehicle price quotes info from raw email messages
* Vehicle price quote database

Along with this release,  version of the underlying reader bot is also upgraded to v1.0.0.  Below are specs for the API

* End point: `/api/v2/handle_text_api_call`
* Accepted Method: post
* Input: text, html or URL
* Output: whether the input text has vehicle price quotes or not, if so list of vehicle price quotes, whether or not the input text has dealer info, if so the info of dealer, metadata of input
* Output format: json