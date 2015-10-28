# MediaConch Matroska Survey

## Introduction

This repository contains a research corpus used in the development of the [MediaConch](https://mediaarea.net/MediaConch). These collections contain MediaArea XML documents which contain both a [MediaInfo](https://mediaarea.net/en/MediaInfo) report and a [MediaTrace](https://mediaarea.net/mediatrace) report. Between these reports most of the structure of Matroska files is documented along with a list of significant characteristics of the file.

Whenever an XML file exceeds a size of 2 megabytes, the file is compressed using gzip compression before being added to the repository, which reduces size substantially. To read a gzip compressed file it is recommended to use gzcat, such as:

```
gzcat MatroskaFile.mkv_maxml.xml.gz | grep "<CompleteName>"
```

Because the majority of the structure of a Matroska is used within the Cluster elements, there may also appear a file with a "_nocluster" suffix. This xml report is the same as its neighboring xml but has all MediaTrace elements that document the Cluster elements removed. This allows nearly every sample to be documented by an xml file that can be under 2 MB in size.

For instance the file at [(1919) Das Cabinet des Dr. Caligari.mkv_maxml.xml.gz](https://github.com/dericed/MediaConch_MKVSurvey/blob/master/archive_org/1919DasCabinetDesDr.Caligari/%281919%29%20Das%20Cabinet%20des%20Dr.%20Caligari.mkv_maxml.xml.gz) represents a gzipped archive of a MediaArea XML containing both a MediaInfo and MediaTrace report on a Matroska file of Das Cabinet Des Dr. Caligari. The file called [(1919) Das Cabinet des Dr. Caligari.mkv_maxml.xml_cluster.xml](https://github.com/dericed/MediaConch_MKVSurvey/blob/master/archive_org/1919DasCabinetDesDr.Caligari/%281919%29%20Das%20Cabinet%20des%20Dr.%20Caligari.mkv_maxml.xml_nocluster.xml) presents the same report but without the reporting on the Matroska Cluster elements within MediaTrace.

## Collections

### archive_org

The [archive.org](archive_org) collection consists of Matroska files identified in the public collections of [archive.org](https://archive.org). Within this collection each subdirectory represents an Internet Archive asset identifier with each file within that being named after the source file of that asset.
