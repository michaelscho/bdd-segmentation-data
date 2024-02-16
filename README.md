# bdd-segmentation-data
This dataset comprises of PageXML for training segmentation models in Kraken that can be used 
to capture the specific layout of medieval canon law collections. Therefore, it has been compiled 
from several 11th century manuscript of the Decretum Burchardi as part of an ongoing edition 
project (Burchards Dekret Digital). Annotations follow project specific needs, but can be adapted
to other usecases. Data was first prepared using Transkribus, and then remasked in escriptorium
for usage in kraken. PageXML of each manuscript has its own folder using a sigla sytsem that is
explained below. For copyright reasons, each folder contains an url mapping as JSON file, 
containing the link to images of each page a sprovided by a library. 
Before usage, these files must be downloaded. For most manuscripts, the url specified already points 
to the resolution used for PageXML creation via iiif url. Manuscript E, however, must be resized 
to the resolution given in the corresponding PageXML files.

## Scope
As collections of medieval canon law often follow a specific layout meant to facilitate legal 
practices, the dataset (and models derived from it) tries to capture the function of layout 
elements in this narrow context. Thus, annotation is based on a context specific vobabulary
consisting of seven region types:

* column_1
* column_2
* inscription
* chapter_count
* header
* footer
* other

[BILD]

As only these values are used, dataset can be adapted to other usecases by regex. Be aware, as
this dataset has been created with a very specific codicological context in mind, other usecases
will most certainly require additonal data.

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
