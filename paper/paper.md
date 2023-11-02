---
title: 'Rendering co-author graphs using linked-open-data from Wikidata'
title_short: 'BioHackEU23 #26: Wikidata driven co-author graphs'
tags:
  - wikidata
  - co-citation graphs
  - Scholia
authors:
  - name: Egon Willighagen
    orcid: 
    affiliation: 1
  - name: Andra Waagmeester
    orcid: 0000-0000-0000-0000
    affiliation: 2
affiliations:
  - name: First Affiliation
    index: 1
  - name: Micelio BV
    index: 2
date: 8 November 2023
cito-bibliography: paper.bib
event: BH23EU
biohackathon_name: "BioHackathon Europe 2023"
biohackathon_url:   "https://biohackathon-europe.org/"
biohackathon_location: "Barcelona, Spain, 2023"
group: Project 26
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/biohackrxiv/publication-template
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: First Author \emph{et al.}
---


# Introduction
Wikidata is the linked-open-data graph of the Wikimedia foundation with its most known sibling Wikipedia. What Wikipedia
is to text, Wikidata is to data. Like in Wikipedia linked-data can be added for everyone, by everyone. This makes Wikidata
a very rich source of data.
A substantial part of the data on Wikidata is about scientific publications and the authors of these publications. Scholia
is a tool that uses this data to create a profile page for authors and publications. 
This report describes a workflow to create co-author graphs using the data from Scholia. 

# Workflow
Figure 1 shows an example of a co-participation graph of this edition of the BioHackathon Europe 2023 at the time of writing 
of this report. The graph is created using data from Wikidata, which is used by Scholia to create the profile pages of the individual
participants and the overall event page. 
This graph currently lists only the participants that have a Wikidata item, that also lists their participationt to the
Biohackathon.
The following steps can be taken to add a participant to this graph:
1. Create a Wikidata item for the participant. This requires an ORCID. First search Wikidata to see if you are not already added to Wikidata. If not, [create a new Wikidata item](https://www.wikidata.org/wiki/Special:NewItem).
    add as much information as you can, but at least the following statements:add your ORCID and name.
   1. Add a statement that you are a person. This can be done by adding the following statement: instance of (P31) human (Q5).
   2. Add a statement that you have an ORCID. This can be done by adding the following statement: ORCID iD (P496) and your ORCID.
   3. Complete the header of the Wikidata item with your name and provide a very short description of yourself (e.g. biocurator, data steward).
   4. (optional) Complete the header of the Wikidata item in multiple languages. 
2. (Optional) Upload a photo of yourself to [Wikimedia Commons](https://commons.wikimedia.org/wiki/Special:UploadWizard). This needs to be a photo of which you own the rights to share. 
3. Add the following statemnts to Wikidata item:
    1. Add a statement that you are a participant of the BioHackathon Europe 2023. This can be done by adding the following statement: BioHackathon Europe 2023 (Q118733318) (or other event item)
    Navigate to the [participant statement](https://www.wikidata.org/wiki/Q118733318#P710) (P710)
    And add yourself, either by typing your name using autocompletion or add the Wikidata identifier of the Wikdata item that represents your profile
   2. (optional) Add a statement that points to your photo on Wikimedia Commons. This can be done by adding the following statement: image (P18) and the identifier of the image on Wikimedia Commons.

Navigate to the [BioHackathon Europe 2023](hhttps://scholia.toolforge.org/event/Q118733318) page on Scholia.
You should now see your name and photo appear on the page.
If you click on your name you will be taken to your profile page on Scholia. On this page you will see a list of your publications and co-authors.

# Formatting

This document use Markdown and you can look at [this tutorial](https://www.markdowntutorial.com/).

## Subsection level 2

Please keep sections to a maximum of only two levels.

## Tables and figures

Tables can be added in the following way, though alternatives are possible:

Table: Note that table caption is automatically numbered and should be
given before the table itself.

| Header 1 | Header 2 |
| -------- | -------- |
| item 1 | item 2 |
| item 3 | item 4 |

A figure is added with:

![Caption for BioHackrXiv logo figure](./biohackrxiv.png)

# Other main section on your manuscript level 1

Lists can be added with:

1. Item 1
2. Item 2

# Citation Typing Ontology annotation

You can use [CiTO](http://purl.org/spar/cito/2018-02-12) annotations, as explained in [this BioHackathon Europe 2021 write up](https://raw.githubusercontent.com/biohackrxiv/bhxiv-metadata/main/doc/elixir_biohackathon2021/paper.md) and [this CiTO Pilot](https://www.biomedcentral.com/collections/cito).
Using this template, you can cite an article and indicate _why_ you cite that article, for instance DisGeNET-RDF [@citesAsAuthority:Queralt2016].

The syntax in Markdown is as follows: a single intention annotation looks like
`[@usesMethodIn:Krewinkel2017]`; two or more intentions are separated
with colons, like `[@extends:discusses:Nielsen2017Scholia]`. When you cite two
different articles, you use this syntax: `[@citesAsDataSource:Ammar2022ETL; @citesAsDataSource:Arend2022BioHackEU22]`.

Possible CiTO typing annotation include:

* citesAsDataSource: when you point the reader to a source of data which may explain a claim
* usesDataFrom: when you reuse somehow (and elaborate on) the data in the cited entity
* usesMethodIn
* citesAsAuthority
* citesAsEvidence
* citesAsPotentialSolution
* citesAsRecommendedReading
* citesAsRelated
* citesAsSourceDocument
* citesForInformation
* confirms
* documents
* providesDataFor
* obtainsSupportFrom
* discusses
* extends
* agreesWith
* disagreesWith
* updates
* citation: generic citation


# Results


# Discussion

...

## Acknowledgements

...

## References
