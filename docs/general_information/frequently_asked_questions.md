---
tags: [ about ]
title: AGDR FAQs
description: ""
---

# Frequently Asked Questions

## What is the AGDR metadata model?
The metadata model for AGDR can be viewed at https://data.agdr.org.nz/DD.  This bespoke metadata dictionary was built incorporating existing standards, such as the Genomics Standards Consortium's Minimum Information about any (x) Sequence (MIxS, https://www.gensc.org/pages/projects/mixs-gsc-project.html) (Field et al., 2008; Wooley et al., 2009) and several relevant fields derived from the Biodiversity Information Standards Organization (TDWG, https://dwc.tdwg.org/) “Darwin Core Standard” (Wieczorek et al., 2012) while also incorporating unique aspects such as the data governance considerations and the adoption of Biocultural Labels and Notices (Anderson & Hudson, 2020). 
Developing this dictionary included several community workshops to further determine what features researchers in Aotearoa New Zealand felt were needed. We are always looking for feedback and can adapt the dictionary to meet new or additional use cases, so please get in touch if you feel you have additional requirements. 

## What is a project?
Fundamentally a research project is a unique systematic and organized investigation conducted to answer research questions or objectives. In AGDR we let researcher’s define what is covered by a single project, but it tends to relate to units based firstly on topic then on aspects such as Kaitiaki, funding and/or publication. 

## What is a dataset?
A dataset is a single collection of data within a project. There may be a single or multiple datasets within a project. Again this is researcher defined, though we are happy to make recommendations if you wish. Each dataset should have a Kaitiaki responsible for 

## How do I know which fields to complete?
You should complete as much metadata as is relevant to your project, however this is unlikely to be all fields. The fields highlighted green in the metadata template are mandatory so please ensure you complete all of these as a minimum. 

## I don’t have the information for some of the mandatory fields
This is fine, many of the mandatory fields can accept ‘unknown’ as the value. If you are unsure, you are welcome to ask us, regardless we will check the answers are valid with a validation tool and be in contact if we need to check anything with you as part of the ingest process.  

## What is the difference between genome and sample?
The metadata dictionary is designed to allow for different experimental designs. The genome tab refers to information about the individual being sampled. For example the individual kākāpō, its development stage, sex etc while the sample tab would be information about the sample taken from that individual for sequencing. So for example a blood sample and how that blood was stored and subsequently used. This allows for longitudinal studies to be included, where samples from the same individual are collected over months or years.

## What is the difference between metagenome and sample?
The metadata dictionary is designed to allow for different experimental designs. The genome tab refers to information about the individual being sampled. For example the individual kākāpō, its development stage, sex etc while the sample tab would be information about the sample taken from that individual for sequencing. So for example a blood sample and how that blood was stored and subsequently used. This allows for longitudinal studies to be included, where samples from the same individual are collected over months or years.

## How do I find the file size?
The command du -h will give the file size, parameters such as the depth reporting can also be set e.g. du -h --max-depth=1

## How do I generate the file md5 checksums?
Please generate a md5 checksum for each file you intend to upload. These should be generated from the most original copy of the file
Sequencing providers often provide the md5 checksum for each file. Please use this checksum where possible
To generate the md5 checksum, please see the NeSI docs: https://docs.nesi.org.nz/Scientific_Computing/Running_Jobs_on_Maui_and_Mahuika/Checksums/

## Why do I need to generate file checksums?
Using the hash generated from a checksum will allow users to check the integrity of a file. This is particularly important as divergences from the original file could occur without being noticed. Common examples where this could happen are files being corrupted over long or unstable file transfers, accidental modification of a file. Files that are identical will produce the same checksum, by checking the checksum of a file, you can see if it has deviated from the file that the checksum was generated from. It is therefore important to use the most original data source to generate the checksum. 

## How do I get the checksums?
Please see the NeSI docs https://docs.nesi.org.nz/Scientific_Computing/Running_Jobs_on_Maui_and_Mahuika/Checksums/
