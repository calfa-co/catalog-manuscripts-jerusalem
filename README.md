# Catalog of Armenian Manuscripts of Jerusalem

This repository contains the structured bibliographic data for the **Jerusalem Armenian Manuscript Catalogue**, digitized as part of the CALFA manuscript catalog project.

The data are intended to be used by the unified CALFA manuscript catalogue website together with the Vienna and Venice collections.

## Collection

- **Collection:** Jerusalem
- **Public manuscript ID prefix:** `J`
- **Volumes:** 11
- **Catalogue notice groups identified:** 3,827
- **Records currently complete through the automated extraction/refinement pipeline:** 3,768
- **Records requiring human review:** 59

A public manuscript identifier is constructed from the catalogue `numero`:

```text
numero: 3171
public ID: J3171

The public ID is distinct from internal processing identifiers and from no_notice.
Repository structure
The intended structure of the repository is:
catalog-manuscripts-jerusalem/
├── records/
│   ├── J1.json
│   ├── J2.json
│   ├── J3.json
│   └── ...
├── catalog.json
└── README.md

records/
Contains one structured JSON record per manuscript.
Example:
records/J3171.json

catalog.json
Provides a consolidated index of the Jerusalem records for use by the CALFA catalogue website and other applications.
Data model
The extracted records preserve the structure and terminology of the printed catalogue.
Typical fields include:
numero
no_notice
titre
date_debut
date_fin
details_date
lieu_copie
reference
genre_id

nb_pages
dimensions
mise_en_page
details_ecriture
types_cahiers
details_matiere
nb_lignes
reliure
etat_conservation

copiste
possesseur
commanditaire
enlumineur
relieur
traducteur

page_garde_parchemin
lettrines
initiales
enluminures_marginales
images
table_canons_1
table_canons_2
decorations

titres_texte
pages_blanches
colophon
informations_diverses
contenu

Some records may contain additional collection-specific fields.
Internal extraction metadata such as _meta and _refine are processing information and are not part of the scholarly catalogue record exposed by the public interface.
Methodology
The catalogue was processed through a multi-stage extraction pipeline.
The workflow includes:
1. identification of manuscript notice boundaries;
2. OCR / visual-language-model transcription;
3. structured extraction into catalogue fields;
4. refinement and verification against the original catalogue pages;
5. automated quality-control checks;
6. targeted human review for unresolved or ambiguous cases.
The extraction process preserves the wording of the source catalogue as closely as possible rather than rewriting or modernizing the catalogue text.
Quality control
A distinction is maintained between:
- records complete through the automated processing pipeline;
- records requiring targeted human review;
- internal QA and processing metadata.
The public catalogue does not present an artificial confidence score for individual records.
Instead, the final catalogue interface is designed to allow researchers to:
- consult the structured record;
- inspect the corresponding source catalogue images;
- report a typo or structural error;
- submit corrections through GitHub Issues.
This repository should therefore remain the source of truth for corrected Jerusalem catalogue data.
Source images
Catalogue page images are not stored in this Git repository.
Images are maintained separately in object storage and are linked to manuscript records by the public catalogue website.
The image collection contains the eleven Jerusalem volumes:
Jerusalem_V1
Jerusalem_V2
Jerusalem_V3
Jerusalem_V4
Jerusalem_V5
Jerusalem_V6
Jerusalem_V7
Jerusalem_V8
Jerusalem_V9
Jerusalem_V10
Jerusalem_V11

Public catalogue
Jerusalem will be searchable together with the Vienna and Venice manuscript catalogues through the unified CALFA catalogue website:
catalog-manuscripts-website

The common public manuscript identifiers are:
J<number>  Jerusalem
W<number>  Vienna
V<number>  Venice

For example:
J3171
W1305
V726

Corrections and contributions
If you identify a typo, missing text, incorrect field assignment, or another problem in a manuscript record, please open a GitHub Issue.
Please include, whenever possible:
- manuscript ID;
- catalogue number;
- affected field;
- current value;
- proposed correction;
- link to the corresponding source image.
Corrections should be made in the catalogue data repository so that the public website can consume the corrected source data.
Related repositories
calfa-co/catalog-manuscripts-jerusalem
calfa-co/catalog-manuscripts-vienna
calfa-co/catalog-manuscripts-venice
calfa-co/catalog-manuscripts-website

CALFA
CALFA develops tools and digital resources for the study and preservation of Armenian written heritage.
Website:
https://calfa.fr
