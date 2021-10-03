# Validation plan

## Name of device
HippoVolume.AI

## Intended use of the product
The product is intended to be used as an end-to-end AI system having a maching learning algorithm that integrates into a clinical grade viewer and automatically calculates the hippocampal volume for a given study.

## Training data collection
We are using the "Hippocampus" dataset from the [Medical Decathlon competition](http://medicaldecathlon.com/). This dataset is stored as a collection of NIFTI files, with one file per volume, and one file per corresponding segmentation mask. The original images here are T2 MRI scans of the full brain. The radiology department runs a HippoCrop tool which cuts out a rectangular portion of a brain scan from every image series and our committed radiologists have collected and annotated a dataset of relevant volumes.

## Label of training data
The training data has been labeled and verified by in house radiologists.

## Measurement of training performance of the algorithm and real-world performance estimation
The training performance of the algorithm was evaluated by using the following metrics:
* Dice Similarity Coefficient
* Jaccard Distance

The real world performance is estimated by competent radiologists.

## Expected real world algorithm performance based on type  of data
The algorithm is designed to perform well on MRI scans if the hippocampal volume is between 2200 and 4500. It would not perform well if the hippocampal volume lies outside this range.
