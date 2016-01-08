# Public finance

Ukraine's public finance data sources

## Budget

There are different levels of budget data:

 * State budget
 * Region budget
 * City budget

There are different types of budgeted operations:

* revenue
* expenditure (spending)
* transfer
* loan
* loan return
* credit
* credit return

[Fiscal Data Package](http://fiscal.dataprotocols.org/spec/#data-files) tries to define a standard representation of budgeting data.

There are some state budget parsing scripts in this repository: https://github.com/datagovua/budget

## Spending data

Actual spending data can be different from budgeted.
There are different sources of spending data:

* budget execution reports (spending part) - http://www.treasury.gov.ua/main/uk/doccatalog/list?currDir=146477
* public bank transactions data (spending part) - http://spending.gov.ua/
* contracting data

### Public bank transactions data

The following repository contains scripts to download http://spending.gov.ua data:
https://github.com/datagovua/spending-data

## Contracting data

[Open contracting data standard](http://ocds.open-contracting.org/standard/r/1__0__0/en/schema/reference/) defines the following stages of contracting:

* planning (оголошення річних планів закупівель) - будуть завантажені на http://spending.gov.ua/
* tender (проведення процедури закупівлі) - ProZorro API та http://drz.lanet.ua/updates/
* award (оголошення переможця) - ProZorro API та http://drz.lanet.ua/updates/
* contract (підписання договору)
* implementation (виконання робіт, перерахування коштів) - http://spending.gov.ua/

The following repository contains scripts to download procurement data:

https://github.com/datagovua/zakupivli

## Organizations

Any fiscal record has an organizations receiving or spending money along with metadata.

  * id (ЄДПРОУ)
  * name (Офіційна назва)
  * short_name (Коротка назва)
  * address
    * physical (фізична адреса)
    * legal (юридична адреса)
    * email
    * website
  * bank requisites (банківські реквізити)
    * bank name (назва банку)
    * band id (МФО)
    * account (рахунок)

According to [open data act](http://www.kmu.gov.ua/control/uk/cardnpd?docid=248573101) the registry of Legal Entities and Physical Entities-Entrepreneurs should be opened to public before April 2016.

But even now there are multiple sources of organizations involved:

  * Вісник державних закупівель
  * ЦБД ProZorro
  * Edata
