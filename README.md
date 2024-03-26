# bdd-segmentation-data
This dataset comprises PageXML for training segmentation models in Transkribus and Kraken. It is designed to capture the specific layout of medieval canon law collections. Compiled from several 11th-century manuscripts of the Decretum Burchardi, it supports the ongoing edition project Burchards Dekret Digital. Annotations are tailored to project-specific needs but can be adapted for other use cases. The data was first prepared using Transkribus (in the transkribus folder) and then remasked in eScriptorium for usage in Kraken (in the kraken folder). The PageXML of each manuscript is organized in its own folder, following a sigil system explained below. Due to copyright reasons, each folder contains a URL mapping as a JSON file, providing links to images of each page as provided by a library. These files must be downloaded before use. For most manuscripts, the specified URL already points to the resolution used for PageXML creation via the IIIF URL. However, Manuscript E must be resized to the resolution given in the corresponding PageXML files.

[![DOI](https://zenodo.org/badge/758361114.svg)](https://zenodo.org/doi/10.5281/zenodo.10882816)

## Scope

As collections of medieval canon law often follow a specific layout meant to facilitate legal practices, this dataset (and the models derived from it) aims to capture the function of layout elements within this narrow context. Annotations are based on a context-specific vocabulary consisting of seven region types:

* column_1
* column_2
* inscription
* chapter_count
* header
* footer
* other

![Example](https://github.com/michaelscho/bdd-segmentation-data/blob/431e1b0c2a251fc66196e9f55e9cc36d3f1c7112/example_annotation.png)

As these values are exclusively used, the dataset can be adapted to other use cases through regex. However, given that this dataset was created with a very specific codicological context in mind, additional data will likely be required for other applications.

## Data
Seven manuscripts are annotated with text regions and baslines:

* B: Bamberg, SB, Msc.Can.6 ([online](https://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb00140701-0)), saec. 11
* E: Eichstätt ,UEI, Cod. st 772 ([online](https://nbn-resolving.org/urn:nbn:de:bvb:824-cod-st-772-8)), saec. 11/12 **adaption to resolution necessary**
* F: Frankfurt, UB, Ms. Barth. 50 ([online](https://sammlungen.ub.uni-frankfurt.de/msma/urn/urn:nbn:de:hebis:30:2-12488)), saec. 11
* K: Köln, EDD, Cod. 119 ([online](https://digital.dombibliothek-koeln.de/urn/urn:nbn:de:hbz:kn28-3-3241)), saec. 11
* M1: München, BSB, Clm 5801 c ([online](https://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb00151690-2)), saec. 12
* M2: München, BSB, Clm 18094 ([online](https://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb00151691-8)), saec. 12
* V: Vatican, BAV, Pal.lat.585 ([online](https://digi.vatlib.it/mss/detail/Pal.lat.585)), saec. 11

For each manuscripts, imagelinks are listed in json format in each manuscripts folder that can be used for batch downloading.
For E, which is not yet iiif complinat, images must be resized to match resolution indicated in PageXML.

## Contributions
Data was prepared as part of the project [Buchards Dekret Digital](https://www.adwmainz.de/projekte/burchards-dekret-digital/informationen.html),
funded by the [Academy of Sciences and Literature Mainz](https://www.adwmainz.de/).
This dataset was conceptualized, curated, and annotated by 
Michael Schonhardt (Universität Kassel, https://orcid.org/0000-0002-2750-1900). 
Annotation was assisted by Leo Felder (Universität Kassel, https://orcid.org/0009-0008-7230-4229), 
Torben Jordan (Universität Kassel, https://orcid.org/0009-0002-2143-0520) and 
Christopher Oed (Universität Erlangen-Nürnberg, https://orcid.org/0009-0001-3910-1832).
