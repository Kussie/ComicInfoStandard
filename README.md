# ComicInfo.xml Standard (Proposed)

## Purpose
The purpose of this repository is to try and standardise the formatting of the common ComicInfo.xml file used by a number of programs and applications to provide metadata for Comics/Mangas/Manhwa etc.  A Github location for these version would also be helpful in codifying this proposed standard, and allow third party system to utilize them much easier.

## History
The history of this file stems from use in the application ComicRack, there has never been a defined strong standard definition of what should be contained in this file, there is at least two known versions, which have been included and tagged in this repository as 1.0 and 2.0

This file has been adopted by many downloaders, libraries and applications since it's inception, and some of these have made their own changes to it resulting in what can be a bit of a headache in its support in various different places.

## Anansi Project
A worthy project trying to push and adopt a standard format for metadata across comics/mangas https://github.com/anansi-project/rfcs


## Proposal
### 3.0
The main goal of 3.0 is to try to move it further away from being tailored to Manga and more generic usage allowing potential adoption for comics, graphic novels and others.
* Removed isManga field and replaced with a more generic `Type` field
* Added a field for series synonyms `SeriesAlsoKnownAs`
* Added `Tags` field for a list of tags, which are usually treated separately to genres.
* Added a `Rating` decimal field to hold the value of a rating (Usually from third party source and rated out of 10)
* Added a `ReadingDirection` field
* Simplified range of known `AgeRating`
* Added a boolean field `Licensed` that determines whether something has been licenced by a known publisher
* Added a field `LicensedPublisher` that can store the name of the licenced publisher
* Added `SchemaVersion` to the `ComicInfo` element to specify a template version
* Added `SchemaTemplate` to the `ComicInfo` element to specify a url to the defined template