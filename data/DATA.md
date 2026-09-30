# Data availability
## English
For data access, please use contact:\
**Aysegul Gunduz (corresponding author)**\
    Department of Biomedical Engineering\
    University of Florida\
    1275 Center Dr.\
    Biomedical Sciences Building, J283\
    Gainesville, FL 32611\
    Email: agunduz@bme.ufl.edu

Expected layout after you obtain data:
```
raw_data/
     subject_number/date_of_visit/
                                Left_IPG/*.json     # LFP data
                                Right_IPG/*.json
                                VideoLabels/*.mat  # corresponding video labels synchronized to EMG via TTL pulse
```

Then run the `perceive` function to load your `*.json` files from Medtronic Percept PC/RC and the analysis scripts as described in README.md.
