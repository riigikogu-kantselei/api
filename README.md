# Avaandmete API

Avaandmed on masinloetavas vormingus andmed, mis on antud kõigile kasutamiseks. Sellelt lehelt leiate info, kuidas kasutada Riigikogu veebilehega seotud avaandmeid. Ligipääs avaliku sektori avaandmetele on infoühiskonna üks põhiõigusi ja sellel on oluline mõju riigi juhtimise läbipaistvusele, kodanike kaasamisele, majanduse elavdamisele, teadusuuringute tegemisele, avaliku sektori tõhustamisele jne. Avaandmete kasutamisel nõustute [Creative Commons 3.0 BY-SA](https://creativecommons.org/licenses/by-sa/3.0/ee/legalcode) litsentsitingimustega.

Riigikogu Kantselei avaandmete teenused võimaldavad IT-asjatundjale paindlikku ja kohest ligipääsu töö käigus tekkinud infole. Avaandmeid väljastatakse läbi rakendusliidese (API) JSON-vormingus. Avaandmete APIt saab kasutada [api.riigikogu.ee](https://api.riigikogu.ee/) kaudu. Paljud andmed on API väljundites esitatud universaalsete ja unikaalsete identifikaatoritena (UUID), millele saab selgitava vaste sobiva API päringu tegemisel.

Näiteks 2013. aasta 15. jaanuari täiskogu istungil toimunud hääletuste vaatamiseks saab kasutada teenust /api/votings. Päringu URLi koostamisel tuleb lisada soovitud perioodi algus- ja lõpukuupäeva parameetrid, vastavalt startDate (aaaa-kk-pp) ning endDate (aaaa-kk-pp). Selles näites on parameetrid ”2013-01-15” ja päring ise näeb välja selline: [https://api.riigikogu.ee/api/votings?startDate=2013-01-15&endDate=2013-01-15&lang=et](https://api.riigikogu.ee/api/votings?startDate=2013-01-15&endDate=2013-01-15&lang=et). Tehtud päringu väljundiks on valitud ajavahemikul toimunud istungite päevakorrapunktide hääletuste üldnimekiri JSON-vormingus.

Kui on soov vaadata konkreetse hääletuse detailandmeid, tuleb näites saadud info alusel teha järgmine päring teenusega /api/votings/{uuid}. Näiteks Riigikogu otsuse ”Ettepaneku tegemine Vabariigi Valitsusele” hääletuse detailandmete päringu tegemiseks tuleb otsida eelnevast vastusest üles selle otsusega seotud hääletuse UUID, milleks on **db57ca8d-7fe4-44cb-ab47-a68e46a683d5**. Päring ise näeb välja selline: [https://api.riigikogu.ee/api/votings/db57ca8d-7fe4-44cb-ab47-a68e46a683d5?lang=et](https://api.riigikogu.ee/api/votings/db57ca8d-7fe4-44cb-ab47-a68e46a683d5?lang=et). Tehtud päringu väljundiks on kõigi Riigikogu liikmete hääletusinfo isikute kaupa.

**NB:** 2012.-st aastast varasemates andmetes võib esineda puudusi. Hetkel ei ole API kaudu failide allalaadimine võimalik.

## Programmivead ja parandusettepanekud

Käesoleva repositooriumi eesmärk on olla avalik raporteerimiskeskond Riigikogu Kantselei [Avaandmete API](https://api.riigikogu.ee/) liidesele. Palume raporteerida kõik leitud vead [avades uue pileti](https://github.com/riigikogu-kantselei/api/issues/new). Tänud.

### Lahtised piletid

[Lahtised piletid](https://github.com/riigikogu-kantselei/api/issues)

### Keel

Peamine töökeel on eesti keel. Teise valikuna võib kasutada inglise keelt.

## Kontakt

Küsimuste korral kirjutage [riigikogu@riigikogu.ee](mailto:riigikogu@riigikogu.ee)

---

# Open data API

Open data means computer readable data that is made accessible to the public. This page explains how to use the open data related to the Riigikogu web page. Access to public sector open data is one of the fundamental rights of the information society and a major factor ensuring the transparency of governance, inclusion of citizens, stimulating economy, scientific research, improving the efficiency of the public sector, etc. Terms and conditions of the [Creative Commons 3.0 BY-SA](https://creativecommons.org/licenses/by-sa/3.0/ee/legalcode) licence apply to the use of open data.

The Chancellery of the Riigikogu open data services allow IT specialists flexible and immediate access to the information generated through work processes. Application programming interface (API) generates data in JSON format. The public data API is accessible via [api.riigikogu.ee](https://api.riigikogu.ee/). Much of the API output data is presented as universal unique identifiers (UUID) which provide an explanatory response only after subsequent API requests.

For example, you can use the /api/votings service to view the votes of the 15 January 2013 plenary sitting.

When compiling the URL of a request, you must enter the start and end date parameters of the requested period, respectively as startDate (yyyy-mm-dd) and endDate (yyyy-mm-dd); in the given example, both would be “2013-01-15“. Your completed request would look like this: [https://api.riigikogu.ee/api/votings?startDate=2013-01-15&endDate=2013-01-15&lang=et](https://api.riigikogu.ee/api/votings?startDate=2013-01-15&endDate=2013-01-15&lang=et), and its output would consist of the general list of votes of items on the agenda during the selected period, in JSON format.

To access detailed information on a particular vote, you must use the information received in the previous example as the basis for making the next request with the service /api/votings/{uuid}. Consequently, to request detailed data on the vote on “Making a Proposal to the Government of the Republic”, you must first find the UUID of the vote from the previous reply, which is **db57ca8d-7fe4-44cb-ab47-a68e46a683d5**. The request itself would look like this: [https://api.riigikogu.ee/api/votings/db57ca8d-7fe4-44cb-ab47-a68e46a683d5?lang=et](https://api.riigikogu.ee/api/votings/db57ca8d-7fe4-44cb-ab47-a68e46a683d5?lang=et), and its output would consist of the individualised voting information of all the members of the Riigikogu.

**NB:** Data earlier than 2012 may be defective. At the moment, it is not possible to download files using API.

## Bugs and Requests

The purpose of this repository is to work as the public issue tracker for the Chancellery of the Riigikogu's [Open data API](https://api.riigikogu.ee/). If you've found a bug in the API, or have ideas on how we could improve it, please [create an issue](https://github.com/riigikogu-kantselei/api/issues/new). It's greatly appreciated.

### Open issues

[Open tickets](https://github.com/riigikogu-kantselei/api/issues)

### Language

Main working language for tickets is Estonian. English may be used as a secondary option.

## Contacts

If you have any further questions, please do not hesitate to contact us at [riigikogu@riigikogu.ee](mailto:riigikogu@riigikogu.ee)
