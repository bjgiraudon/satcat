# SATCAT Extension Specification

- **Title:** SATCAT
- **Identifier:** <https://github.com/bjgiraudon/satcat/raw/refs/tags/v1.0.0/json-schema/schema.json>
- **Field Name Prefix:** satcat
- **Scope:** Item, Collection
- **Extension [Maturity Classification](https://github.com/radiantearth/stac-spec/tree/master/extensions/README.md#extension-maturity):** Proposal
- **Owner**: @bjgiraudon

This document explains the SATCAT Extension to the [SpatioTemporal Asset Catalog](https://github.com/radiantearth/stac-spec) (STAC) specification.

The Satellite Catalog Number (SATCAT), also known as NORAD Catalog Number, NORAD ID, USSPACECOM object number, is a sequential nine-digit number assigned by the United States Space Command (USSPACECOM), and previously the North American Aerospace Defense Command (NORAD), in the order of launch or discovery to all artificial objects in the orbits of Earth and those that left Earth's orbit. For example, catalog number 1 is the Sputnik 1 launch vehicle, with the Sputnik 1 satellite having been assigned catalog number 2.

Objects that fail to orbit or orbit for a short time are not catalogued. The minimum object size in the catalog is 10 centimetres (3.9 in) in diameter.

- Examples:
  - [Item example](examples/item.json): Shows the basic usage of the extension in a STAC Item
  - [Collection example](examples/collection.json): Shows the basic usage of the extension in a STAC Collection
- [JSON Schema](json-schema/schema.json)
- [Changelog](./CHANGELOG.md)

## Fields

The fields in the table below can be used in these parts of STAC documents:

- [ ] Catalogs
- [x] Collections
- [x] Item Properties (incl. Summaries in Collections)
- [x] Assets (for both Collections and Items, incl. Item Asset Definitions in Collections)
- [ ] Links

| Field Name         | Type   | Description                                    |
| ------------------ | ------ | ---------------------------------------------- |
| satcat:norad       | string | **REQUIRED**. Object's NORAD unique identifier |
| satcat:satname     | string | **REQUIRED**. Object's name                    |
| satcat:object_type | string | **REQUIRED**. Object type                      |
| satcat:country     | string | Country the object belongs  to                 |
| satcat:launch_site | string | Site the object was launched from              |

### Additional Field Information
#### Object type

The object type describes the nature of the artificial object orbiting the Earth.
Current possible values include `PAYLOAD`, `ROCKET BODY` and `DEBRIS`.

#### Country
Below is a subset of the most common SATCAT country codes and their full description.

| Code | Country                                                                 |
| ---- | ----------------------------------------------------------------------- |
| ATF  | French Southern Territories                                             |
| BEL  | BELGIUM                                                                 |
| BRAZ | BRAZIL                                                                  |
| CA   | CANADA                                                                  |
| CHN  | China                                                                   |
| CIS  | COMMONWEALTH OF INDEPENDENT STATES                                      |
| ESA  | EUROPEAN SPACE AGENCY                                                   |
| ESRO | EUROPEAN SPACE RESEARCH ORGANIZATION                                    |
| EUME | EUROPEAN ORGANIZATION FOR THE EXPLOITATION OF METEOROLOGICAL SATELLITES |
| EUTE | EUROPEAN TELECOMMUNICATIONS SATELLITE ORGANIZATION (EUTELSAT)           |
| FGER | FRANCE/GERMANY                                                          |
| FR   | FRANCE                                                                  |
| FRG  | FEDERAL REPUBLIC OF GERMANY                                             |
| FRIT | FRANCE/ITALY                                                            |
| FRRG | FRANCE/FEDERAL REPUBLIC OF GERMANY                                      |
| GER  | GERMANY                                                                 |
| GUF  | French Guiana                                                           |
| IM   | INTERNATIONAL MARITIME SATELLITE ORGANIZATION (INMARSAT)                |
| INMA | INTERNATIONAL MARITIME SATELLITE ORGANIZATION (INMARSAT)                |
| IOT  | British Indian Ocean Territory                                          |
| ISRO | INDIA SPACE RESEARCH ORGANIZATION                                       |
| ISS  | INTERNATIONAL SPACE STATION                                             |
| IT   | ITALY                                                                   |
| ITSO | INTERNATIONAL TELECOMMUNICATIONS SATELLITE ORGANIZATION (INTELSAT)      |
| NATO | NORTH ATLANTIC TREATY ORGANIZATION                                      |
| NETH | NETHERLANDS                                                             |
| NKOR | NORTH KOREA                                                             |
| ORB  | ORBITAL TELECOMMUNICATIONS SATELLITE (GLOBALSTAR)                       |
| PRC  | PEOPLES REPUBLIC OF CHINA                                               |
| PRES | PEOPLES REPUBLIC OF CHINA/EUROPEAN SPACE AGENCY                         |
| RASC | REGIONAL AFRICAN SATELLITE COMMUNICATIONS ORG                           |
| SES  | SOCIÉTÉ EUROPÉENNE DES SATELLITES                                       |
| TBD  | TO BE DETERMINED/UNKNOWN                                                |
| UAE  | UNITED ARAB EMIRATES                                                    |
| UK   | UNITED KINGDOM                                                          |
| UNKN | UNKNOWN                                                                 |
| US   | UNITED STATES OF AMERICA                                                |
| USBZ | UNITED STATES/BRAZIL                                                    |
| USSR | UNION OF SOVIET SOCIALIST REPUBLICS                                     |

#### Launch site
Below is an exhaustive table of the SATCAT launch codes and their full description.

| Code  | Launch site                                    |
| ----- | ---------------------------------------------- |
| AFETR | AIR FORCE EASTERN TEST RANGE                   |
| AFWTR | AIR FORCE WESTERN TEST RANGE                   |
| CAS   | Pegasus launched from Canary Islands Air Space |
| ERAS  | Pegasus launched from Eastern Range Air Space  |
| FRGUI | FRENCH GUIANA                                  |
| HGSTR | HAMMA GUIRA SPACE TRACK RANGE                  |
| JJSLA | Jeju Sea Launch Area                           |
| JSC   | Jiuquan Satellite Launch Center, China         |
| KODAK | Kodiak Island, Alaska                          |
| KSCUT | KAGOSHIMA SPACE CENTER UNIVERSITY OF TOKYO     |
| KWAJL | Kwajalein                                      |
| KYMTR | KAPUSTIN YAR MISSILE AND SPACE COMPLEX         |
| NSC   | Naro Space Center, South Korea                 |
| OREN  | Orenburg, Russia                               |
| PKMTR | PLESETSK MISSILE AND SPACE COMPLEX             |
| PMRF  | Pacific Missile Range Facility                 |
| RLLC  | Rocket Lab Launch Complex                      |
| SADOL | Submarine Launch from Barents Sea, Russia      |
| SCSLA | South China Sea Launch Area                    |
| SEAL  | SEA LAUNCH                                     |
| SEM   | Semnan, Iran                                   |
| SMTS  | Sharud Missile Test Site                       |
| SNMLP | SAN MARCO LAUNCH PLATFORM                      |
| SRI   | SIRHARIKOTA                                    |
| SVOB  | Svobodny, Russia                               |
| SWAS  | SPACEPORT CORNWALL AIR SPACE                   |
| TNSTA | TANEGASHIMA SPACE CENTER                       |
| TSC   | Taiyaun Space Center, China                    |
| TTMTR | TYURATAM MISSILE AND SPACE COMPLEX             |
| UNKN  | Unknown                                        |
| VOSTO | VOSTOCHNY COSMODROME                           |
| VOWAS | Virgin Orbit Western Air Space                 |
| WLPIS | WALLOPS ISLAND                                 |
| WOMRA | WOOMERA                                        |
| WRAS  | Pegasus launched from Western Range Air Space  |
| WSC   | Wenchang Satellite Launch Center               |
| XSC   | Xichang Space Center, China                    |
| YAVNE | Yavne, Israel                                  |
| YSLA  | Yellow Sea Launch                              |


## Contributing

All contributions are subject to the
[STAC Specification Code of Conduct](https://github.com/radiantearth/stac-spec/blob/master/CODE_OF_CONDUCT.md).
For contributions, please follow the
[STAC specification contributing guide](https://github.com/radiantearth/stac-spec/blob/master/CONTRIBUTING.md) Instructions
for running tests are copied here for convenience.

### Running tests

The same checks that run as checks on PR's are part of the repository and can be run locally to verify that changes are valid. 
To run tests locally, you'll need `npm`, which is a standard part of any [node.js installation](https://nodejs.org/en/download/).

First you'll need to install everything with npm once. Just navigate to the root of this repository and on 
your command line run:
```bash
npm install
```

Then to check markdown formatting and test the examples against the JSON schema, you can run:
```bash
npm test
```

This will spit out the same texts that you see online, and you can then go and fix your markdown or examples.

If the tests reveal formatting problems with the examples, you can fix them with:
```bash
npm run format-examples
```
