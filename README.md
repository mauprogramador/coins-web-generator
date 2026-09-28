# COinS Web Generator

<p align="center">
  <img src="./static/img/favicon.ico" width="60" alt="Logo">
</p>
<p align="center">
  <em>Web-based tool to generate COinS metadata for bibliographic references</em>
</p>
<p align="center">
  <a href="https://github.com/mauprogramador/coins-web-generator/releases/latest">
    <img src="https://img.shields.io/github/v/tag/mauprogramador/coins-web-generator?logo=github&label=Release&color=E9711C" alt="Latest Release">
  </a>
  <img src="https://img.shields.io/badge/HTML-E34F26?logo=html5&logoColor=FFF" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS-663399?logo=css&logoColor=FFF" alt="CSS3">
  <img src="https://img.shields.io/badge/JS-F7DF1E?logo=javascript&logoColor=000" alt="JS">
</p>
<p align="center">
  <a href="https://picocss.com/">
    <img src="https://img.shields.io/badge/Pico-13171F" alt="Pico">
  </a>
  <a href="https://prismjs.com/">
    <img src="https://img.shields.io/badge/Prism-FFFFFF" alt="Prism">
  </a>
</p>

---

▶️ Get Started: <https://mauprogramador.github.io/coins-web-generator>

📖 Read the Wiki: <https://github.com/mauprogramador/coins-web-generator/wiki>

<br>

## Overview

**ContextObjects in Spans** (**COinS**) is a method to **embed bibliographic metadata in the HTML** code of web pages. This allows bibliographic software to publish machine-readable bibliographic items and client reference management software to **retrieve bibliographic metadata**.

We will follow the [ANSI/NISO Z39.88-2004](https://www.niso.org/publications/z3988-2004-r2010) (OpenURL 1.0) standard, based on KEV formats and registered registries (including [DCMI](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/)). Version of the ContextObject: **Z39.88-2004**.

_Example:_

```html
<span
  class="Z3988"
  title="ctx_ver=Z39.88-2004&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Ajournal&amp;rft.issn=1045-4438"
></span>
```

<br>

## Metadata Formats

Below are the five core formats containing the majority of fields that remain highly relevant.

### 1. Journal

_Format URI:_ [`info:ofi/fmt:kev:mtx:journal`](https://web.archive.org/web/20181120130531/http://www.openurl.info/registry/docs/info:ofi/fmt:kev:mtx:journal)

| Key           | Name                              |
| ------------- | --------------------------------- |
| `ctx_ver`     | Context Version (`Z39.88-2004`)   |
| `rft_val_fmt` | Format URI                        |
| `rft.genre`   | Genre                             |
| `rft.atitle`  | Article / Paper Title             |
| `rft.jtitle`  | Journal / Publication Title       |
| `rft.aulast`  | Primary Author Last Name          |
| `rft.aufirst` | Primary Author Given Name         |
| `rft.au`      | Full Author Name                  |
| `rft.aucorp`  | Corporate / Organizational Author |
| `rft.date`    | Date (Year)                       |
| `rft_id`      | Identifier (URI / URL / ID / DOI) |
| `rft.volume`  | Volume                            |
| `rft.issue`   | Issue                             |
| `rft.spage`   | Start Page                        |
| `rft.epage`   | End Page                          |
| `rft.pages`   | Page Range (Free-text)            |
| `rft.artnum`  | Article Number                    |
| `rft.issn`    | ISSN                              |
| `rft.eissn`   | Eletronic ISSN                    |
| `rft.isbn`    | ISBN                              |

#### 1.1. Genres

| Genre        | Name            |
| ------------ | --------------- |
| `journal`    | Journal         |
| `issue`      | Issue           |
| `article`    | Article / Paper |
| `conference` | Conference      |
| `proceeding` | Proceeding      |
| `preprint`   | Preprint        |
| `unknown`    | Unknown         |

<br>

### 2. Book

_Format URI:_ [`info:ofi/fmt:kev:mtx:book`](https://web.archive.org/web/20181120130531/http://www.openurl.info/registry/docs/info:ofi/fmt:kev:mtx:book)

| Key           | Name                              |
| ------------- | --------------------------------- |
| `ctx_ver`     | Context Version (`Z39.88-2004`)   |
| `rft_val_fmt` | Format URI                        |
| `rft.genre`   | Genre                             |
| `rft.btitle`  | Book Title                        |
| `rft.atitle`  | Chapter/Item Title                |
| `rft.aulast`  | Primary Author Last Name          |
| `rft.aufirst` | Primary Author Given Name         |
| `rft.au`      | Full Author Name                  |
| `rft.aucorp`  | Corporate / Organizational Author |
| `rft.date`    | Date (Year)                       |
| `rft.pub`     | Publisher                         |
| `rft.place`   | Place of Publication              |
| `rft.edition` | Edition                           |
| `rft.series`  | Series Title                      |
| `rft.spage`   | Start Page                        |
| `rft.epage`   | End Page                          |
| `rft.pages`   | Page Range (Free-text)            |
| `rft.issn`    | ISSN                              |
| `rft.isbn`    | ISBN                              |

#### 2.1. Genres

| Genre        | Name                        |
| ------------ | --------------------------- |
| `book`       | Book                        |
| `bookitem`   | Section / Chapter of a Book |
| `conference` | Conference                  |
| `proceeding` | Proceeding                  |
| `report`     | Report / Technical Report   |
| `document`   | General Document            |
| `unknown`    | Unknown                     |

<br>

### 3. Dissertation

_Format URI:_ [`info:ofi/fmt:kev:mtx:dissertation`](https://web.archive.org/web/20181120130531/http://www.openurl.info/registry/docs/info:ofi/fmt:kev:mtx:dissertation)

| Key           | Field                             |
| ------------- | --------------------------------- |
| `ctx_ver`     | Context Version (`Z39.88-2004`)   |
| `rft_val_fmt` | Format URI                        |
| `rft.title`   | Title                             |
| `rft.aulast`  | Primary Author Last Name          |
| `rft.aufirst` | Primary Author Given Name         |
| `rft.au`      | Full Author Name                  |
| `rft.date`    | Date (Year)                       |
| `rft_id`      | Identifier (URI / URL / ID / DOI) |
| `rft.inst`    | Institution                       |
| `rft.advisor` | Advisor                           |
| `rft.tpages`  | Total Pages                       |
| `rft.isbn`    | ISBN                              |
| `rft.degree`  | Degree                            |
| `rft.co`      | Country                           |

<br>

### 4. Patent

_Format URI:_ [`info:ofi/fmt:kev:mtx:patent`](https://web.archive.org/web/20181120130531/http://www.openurl.info/registry/docs/info:ofi/fmt:kev:mtx:patent)

| Key              | Field                             |
| ---------------- | --------------------------------- |
| `ctx_ver`        | Context Version (`Z39.88-2004`)   |
| `rft_val_fmt`    | Format URI                        |
| `rft.title`      | Title                             |
| `rft.invlast`    | Inventor Last Name                |
| `rft.invfirst`   | Inventor Given Name               |
| `rft.inventor`   | Full Inventor Name                |
| `rft.date`       | Date                              |
| `rft_id`         | Identifier (URI / URL / ID / DOI) |
| `rft.assignee`   | Assignee / Owner                  |
| `rft.number`     | Patent Number                     |
| `rft.applnumber` | Application Number                |
| `rft.kind`       | Kind Code                         |
| `rft.co`         | Country                           |

<br>

### 5. Dublin Core (DC)

_Format URI:_ [`info:ofi/fmt:kev:mtx:dc`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/)

| Key               | Field                                             |
| ----------------- | ------------------------------------------------- |
| `ctx_ver`         | Context Version (`Z39.88-2004`)                   |
| `rft_val_fmt`     | Format URI                                        |
| `rft.title`       | Title                                             |
| `rft.creator`     | Primary Creator / Author                          |
| `rft.date`        | Date (Year)                                       |
| `rft_id`          | Identifier (URI / URL / ID / DOI)                 |
| `rft.identifier`  | Identifier (URI / URL / ID / DOI)                 |
| `rft.subject`     | Subject / Topic                                   |
| `rft.description` | Description                                       |
| `rft.publisher`   | Publisher (Host / Organization / Domain)          |
| `rft.contributor` | Contributor                                       |
| `rft.type`        | Type (DCMI-Type)                                  |
| `rft.format`      | Format (MIME Type / Media Type / Extent)          |
| `rft.source`      | Source (URI / URL)                                |
| `rft.language`    | Language                                          |
| `rft.relation`    | Related Resource (URI / URL)                      |
| `rft.coverage`    | Extent / Scope (Location / Period / Jurisdiction) |
| `rft.rights`      | Rights / Legal Ownership (Copyright)              |

#### 5.1. Types

_Types URI:_ [DCMI Type Vocabulary](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#section-7)

- Collection
- Dataset
- Event
- Image
- InteractiveResource
- MovingImage
- PhysicalObject
- Service
- Software
- Sound
- StillImage
- Text

<br>

### About Generic and Custom Formats

We will use the [Dublin Core](#5-dublin-core-dc) format to map **General Document**, **Non-text**, and **Other Metadata** formats by using its **Type** and **Format** keys.

| Category                             | Type                | Format                                                                           |
| ------------------------------------ | ------------------- | -------------------------------------------------------------------------------- |
| Software / Library / Framework / API | Software            | `application/json` <br> `application/javascript` <br> `application/octet-stream` |
| Web API / Web App / Web Service      | Service             | `text/html` <br> `application/json` <br> `application/xml` <br> `text/xml`       |
| Website / Web Page                   | InteractiveResource | `text/html` <br> `application/xhtml+xml`                                         |
| Documentation / Manual               | InteractiveResource | `text/html` <br> `application/pdf` <br> `text/markdown` <br> `text/plain`        |
| Generic                              | Text                | `text/plain` <br> `text/html` <br> `application/pdf` <br> `application/epub+zip` |

> [!TIP]
> Read about MIME/Media Types on [AINA](https://www.iana.org/assignments/media-types).

<br>

### About Deprecated Formats and Fields

We decided to omit the [Scholarly Service Type](https://web.archive.org/web/20181120130531/http://www.openurl.info/registry/docs/info:ofi/fmt:kev:mtx:sch_svc) format, as it is rarely used and our service is intended to describe reference objects (e.g., books, articles, etc.) rather than resolver service definitions. Consequently, we also decided to replace the **Non-text and Other Metadata** format with the [Dublin Core](#5-dublin-core-dc) format, a flexible container that represents the cleanest and most compliant approach. Finally, likewise, many **obsolete, ignored, discontinued, or rarely used OpenURL keys** (e.g., `rft.ssn`, `rft.quarter`, etc.) will also be omitted.

<br>

### Citation

If this work helped you obtain relevant research data, please cite it:

📝 **APA**

```text
Batista, M. d. S. (2026). COinS Web Generator: Web-based tool to generate COinS metadata for bibliographic references (Version 0.0.1) [Web app]. GitHub. https://github.com/mauprogramador/coins-web-generator.
```

📝 **BibTeX**

```bibtex
@misc{batista2026coins,
  author       = {Batista, M. d. S.},
  title        = {COinS Web Generator: Web-based tool to generate COinS metadata for bibliographic references},
  year         = {2026},
  howpublished = {\url{https://github.com/mauprogramador/coins-web-generator}},
  note         = {Web App, v0.0.1. GitHub. Keywords: COinS; OpenURL; Z39.88; Bibliographic References; Bibliographic-metadata; Web App; Citation-generator. MIT License}
}
```

<br>

### Contributing

Contributions are welcome! Please feel free to [open an issue](https://github.com/mauprogramador/coins-web-generator/issues) or [submit a pull request](https://github.com/mauprogramador/coins-web-generator/pulls).

<br>

### References

1. [COinS](https://en.wikipedia.org/w/index.php?title=COinS&oldid=1326727466). (2025). Wikipedia.
1. [Using Zotero to create COinS metadata](https://www.zotero.org/support/dev/exposing_metadata/coins). (2020). Zotero Documentation.
1. [COinS Generator](https://web.archive.org/web/20130403152633/http://generator.ocoins.info/). (2005). [Arquived]. Openly Informatics.
1. [OpenURL COinS: A convention to embed bibliographic metadata in HTML](https://web.archive.org/web/20170424223448/http://ocoins.info/). (2009). [Archived]. OCLC New Jersey.
1. [Z39.88-2004: The OpenURL Framework for Context-Sensitive Services The Key/Encoded-Value (KEV) Format Implementation Guidelines](https://web.archive.org/web/20181120130531/http://epub.mimas.ac.uk/openurl/KEV_Guidelines-200706.html). (2007). [Archived]. Ann Apps, MIMAS, The University of Manchester.

<br>

---

For questions or concerns please contact me at <sir.silvabmauricio@gmail.com>.

📄 [Attributions](./ATTRIBUTIONS.md)
&nbsp;&#8226;&nbsp;
🧾 [License](./LICENSE)
&nbsp;&#8226;&nbsp;
🔖 [Latest Release](https://github.com/mauprogramador/coins-web-generator/releases/latest)
&nbsp;&#8226;&nbsp;
📑 [Changelog](./CHANGELOG.md)
&nbsp;&#8226;&nbsp;
📖 [Wiki](https://github.com/mauprogramador/coins-web-generator/wiki)
