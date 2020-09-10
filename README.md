TITCO-I dataset version 1
=========================

Licence and terms of use
------------------------

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

Note that any use of this dataset is subject to the terms in the
[LICENCE](LICENCE.md) as well as in the [POLICY](policy.md). Read
these carefully before you download or in any way use the data.

Background and summary
----------------------

In this document we present the central characteristics of the TITCO-I
dataset, including the origin of the data and how it was collected.
Along with this document the following files are included in this
repository:

-   titco-I-full-dataset-v1.csv (full dataset)
-   titco-I-limited-dataset-v1.csv (limited dataset, includes a random
    sample of 1000 observations from the full dataset)
-   codebook-titco-I-v1.pdf (descriptors of all variables in the TITCO-I
    dataset)
-   codebook-titco-I-v1.csv (comma separated file of descriptors of all
    variables in the TITCO-I dataset, intended mainly for programmatic
    use)

To familiarize yourself with the data we recommend that you first read
this document (README). Then eyeball the codebook to get a sense of the
data available (codebook-titco-I-v1.pdf). Finally, import the data into
your analysis software of choice (titco-I-dataset-v1.csv). Useful guides
are available at:

-   [Microsoft
Excel](https://support.office.com/en-us/article/Import-or-export-text-txt-or-csv-files-5250ac4c-663c-47ce-937b-339e391393ba)
-   [SPSS](http://www-01.ibm.com/support/docview.wss?uid%3Dswg21480145)
-   [STATA](http://www.stata.com/features/overview/importing-and-exporting-text-delimited-data/)
-   [R](http://www.statmethods.net/input/importingdata.html)

Any comments, questions or feedback is very much appreciated, including
reports of flaws or apparent errors in the data. Please let us know on
martingerdin\@gmail.com or nobsroy\@gmail.com.

Meta-data
---------

``` {.example}
NAME:            TITCO-I dataset 
VERSION:         1
ROWS:            16000
COLUMNS:         193
CELLS:           3088000
NON-EMPTY CELLS: 2108403
SYSTEM-MISSING:  NA
```

Setting
-------

The TITCO-I v1 dataset includes data on 16 000 patients admitted to
four public university hospitals in urban India. The original dataset
included 16 047 patients but 47 patients were deleted from the dataset
for anonymization purposes, see the anonymization section for more
details. At the time of the research Jai Prakash Narayan Apex Trauma
Center (JPNATC), All India Institute of Medical Sciences, New Delhi,
was a dedicated trauma centre with almost 180 beds. King Edward
Memorial hospital (KEM), Mumbai, was a tertiary level hospital with no
dedicated trauma ward. Lokmanya Tilak Municipal General Hospital
(LTMGH), Mumbai was a tertiary level public university hospital with a
dedicated trauma ward with 14 beds. The Institute of Post-Graduate
Medical Education and Research and Seth Sukhlal Karnani Memorial
Hospital (SSKM), Kolkata was a tertiary level public university
hospital, but without a dedicated trauma ward. The cost of care in
these hospitals was nominal and the patients admitted represented
mainly a lower socioeconomic stratum of the population. The first
patient was enrolled in July 2013 and the last patient in
December 2015. The exact enrollment period varied across participating
hospitals.

Design and participant selection
--------------------------------

One dedicated project officer collected data on site for approximately
eight hours, five days per week. The shifts were rotated, so that the
project officers worked morning, evening, and night shifts, and then had
a day off. This way all possible shifts were covered during the course
of a month. Data for patients arriving during the project officers
shifts were collected by direct observation in the area where trauma
patients were received, and the project officers were allowed to ask the
health care staff for values of parameters not entered into the
patient\'s records. For example, if the systolic blood pressure was
measured (the project officer could see it being measured) but was not
documented in the patient record, the project officer was allowed to ask
for its value. Data for patients arriving to hospital outside the
project officers\' shifts were recorded from patient records. These
patients were identified from the nurses\' log books in the emergency
department.

Eligibility criteria
--------------------

Patients of all ages were included if they presented with history of
trauma and were admitted or died between arrival and admission. Patients
with isolated limb injury and patients who were dead on arrival were not
included.

Ethical considerations
----------------------

We obtained ethical approval for the collection of data for the original
research from each of the participating hospitals. The names of the
ethical bodies and reference numbers were Institute Ethics Committee All
India Institute of Medical Sciences (EC/NP-279/2013 RP-Ol/2013),
Institutional Ethics Committee (IEC(I)/OUT/222/14), Ethics Committee of
the Staff and Research Society (IEC/11/13), and IPGME&R Research
Oversight Committee (IEC/279) for JPNATC, KEM, LTMGH, and SSKM
respectively. We applied for a waiver of informed consent, which was
granted by all review boards. The patients included in this study were
all admitted after trauma, often arriving with an altered level of
consciousness and in severe physical and psychological distress. As the
original research involved only collection of routine data and did not
alter the care provided in any way, we and the ethics committees felt
that obtaining informed consent would be to burden the patients or their
relatives unnecessarily. Names, addresses, telephone, social security or
insurance numbers were never collected.

Anonymization
-------------

### Hospital study identification number

The identification number used to identify individual hospitals in the
original dataset has been replaced with a random number, resulting in
four unique values. No key has been retained to allow linkage of new and
old hospital identification numbers.

### Patient study identification number

The identification number used to identify individual patients in the
original dataset has been replaced with a random identification number,
resulting in 16000 unique values. No key has been retained to allow
linkage of new and old patient identification numbers.

### Dates

Dates have been shifted into the future using a random offset for each
patient, preserving time intervals, day of the week and \"approximate
seasonality\", meaning that between zero and five weeks were added to
the original month. To still allow for temporal splitting of the dataset
a sequential number was generated based on the original date of arrival
and stored as the variable seqn. Important to notice is that it is not
possible to use the date variables to calculate, for example, the number
of patients admitted per day. It is also not possible to estimate the
time between two patients being admitted.

### Times

Times have been retained as they were in the original dataset.

### Random deletion of 47 observations

The original dataset included 16047 observations. In this anonymous
version of the data 47 observations have been randomly deleted. This was
done to prevent identification of patients based on the seqn variable
described under Dates above.

### Age

The age variable has been recoded from a continuous variable to an
ordinal variable so that observations with an age \> 89 recorded are
grouped toghether.

### Injury descriptors and codes

A random selection of 1% of injury descriptors entered into each of the
variables e~1~, e~2~, e~3~, e~4~, e~5~, e~6~, e~7~, e~8~, e~9~, e~10~,
e~11~, e~12~, xray~1~, xray~2~, xray~3~, xray~4~, xray~5~, xray~6~,
xray~7~, xray~8~, xray~9~, xray~10~, xray~11~, fast~1~, fast~2~,
fast~3~, fast~4~, fast~5~, fast~6~, fast~7~, fast~8~, fast~9~, fast~10~,
fast~11~, ct~1~, ct~2~, ct~3~, ct~4~, ct~5~, ct~6~, ct~7~, ct~8~, ct~9~,
ct~10~, ct~11~, ct~12~, ct~13~, op~1~, op~2~, op~3~, op~4~, op~5~,
op~6~, op~7~, op~8~, op~9~, op~10~, op~11~ were set to missing.
Corresponding ICD-10 codes were also set to missing. This was done to
prevent identification of patients based on the list of recorded
injuries.

Citation
--------

TITCO collaborators (2017) TITCO dataset version 1

Credits
-------

This dataset is the result of massive efforts from a large number of
people, beside all patients who contributed their data to the original
research. Being named here does not in any way mean that one approve of
the distribution or use of the data, only that one was involved in the
original research resulting in the data being collected. Collaborators
are listed alphabetically by first name.

Amit Gupta, Ashish Jhakal, Debojit Basak, Deen Mohamed Ismail Professor,
Dusu Yabo, Jegadeesa K, Jyoti Kamble, Makhan Lal Saha, Mangesh
Nitnaware, Martin Gerdin, Monty Khajanchi, Nobhojit Roy, Ranganathan
Jothi, Samarendra Nath Ghosh, Sanjeev Bhoi, Santosh Mahindrakar, Santosh
Tirlotkar, Satish Dharap, Shilpa Rao, Veera Kamal, Vineet Kumar.

Change log
==========

``` {.example}
v1: updated with additional anonymization procedures, added credits and
citation
beta: First version of these files

```
