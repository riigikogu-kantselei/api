# Open data API

Open data means computer readable data that is made accessible to the public. This page explains how to use the open data related to the Riigikogu web page. Access to public sector open data is one of the fundamental rights of the information society and a major factor ensuring the transparency of governance, inclusion of citizens, stimulating economy, scientific research, improving the efficiency of the public sector, etc. Terms and conditions of the [Creative Commons 3.0 BY-SA](https://creativecommons.org/licenses/by-sa/3.0/ee/legalcode) licence apply to the use of open data.

The Chancellery of the Riigikogu open data services allow IT specialists flexible and immediate access to the information generated through work processes. Application programming interface (API) generates data in JSON format. The public data API is accessible via [api.riigikogu.ee](https://api.riigikogu.ee/). Much of the API output data is presented as universal unique identifiers (UUID) which provide an explanatory response only after subsequent API requests.

For example, you can use the [/api/votings](https://api.riigikogu.ee/swagger-ui.html#/Hääletused/getVotingsUsingGET) service to view the votes of the 15 January 2013 plenary sitting.

When compiling the URL of a request, you must enter the start and end date parameters of the requested period, respectively as startDate (yyyy-mm-dd) and endDate (yyyy-mm-dd); in the given example, both would be “2013-01-15“. Your completed request would look like this: [https://api.riigikogu.ee/api/votings?startDate=2013-01-15&endDate=2013-01-15&lang=et](https://api.riigikogu.ee/api/votings?startDate=2013-01-15&endDate=2013-01-15&lang=et), and its output would consist of the general list of votes of items on the agenda during the selected period, in JSON format.

To access detailed information on a particular vote, you must use the information received in the previous example as the basis for making the next request with the service [/api/votings/{uuid}](https://api.riigikogu.ee/swagger-ui.html#/Hääletused/getVotingUsingGET). Consequently, to request detailed data on the vote on “Making a Proposal to the Government of the Republic”, you must first find the UUID of the vote from the previous reply, which is **db57ca8d-7fe4-44cb-ab47-a68e46a683d5**. The request itself would look like this: [https://api.riigikogu.ee/api/votings/db57ca8d-7fe4-44cb-ab47-a68e46a683d5?lang=et](https://api.riigikogu.ee/api/votings/db57ca8d-7fe4-44cb-ab47-a68e46a683d5?lang=et), and its output would consist of the individualised voting information of all the members of the Riigikogu.

## Bugs and Requests

The purpose of this repository is to work as the public issue tracker for the Chancellery of the Riigikogu's [Open data API](https://api.riigikogu.ee/). If you've found a bug in the API, or have ideas on how we could improve it, please [create an issue](https://github.com/riigikogu-kantselei/api/issues/new). It's greatly appreciated.

### Open issues

[Open tickets](https://github.com/riigikogu-kantselei/api/issues)


If you have any further questions, please do not hesitate to contact us at [riigikogu@riigikogu.ee](mailto:riigikogu@riigikogu.ee)

