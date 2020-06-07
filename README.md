# scientific-LMS-zscore-app
python program to compute z-scores with LEAD LMS reference values for data-files


## Reference
This code can be used to compute Z-scores of body composition parameters with the reference values for adults published in: 

__Article Title__: Reference values of body composition parameters and visceral adipose tissue (VAT) by DXA in adults aged 18–81 years—results from the LEAD cohort

__DOI__: 10.1038/s41430-020-0596-5, 2019EJCN0971

__Link__: https://www.nature.com/articles/s41430-020-0596-5

__Citation__: Ofenheimer, A., Breyer-Kohansal, R., Hartl, S. et al. Reference values of body composition parameters and visceral adipose tissue (VAT) by DXA in adults aged 18–81 years—results from the LEAD cohort. Eur J Clin Nutr (2020).

and the reference values for children published in:
TODO


## Requirements
This code was written for python 3.7 with the following dependencies:

```requirements
numpy==1.17.2
pandas==0.25.1
scipy==1.3.1
argparse==1.4.0
xlrd==1.2.0
```

## Usage
The code of this repository is provided for scientist and clinicians who want to compute z-scores with our reference LMS-values for multiple individuals at the same time. For single computations we also provide an app which might be easier to use [here](https://leadstudy.at). 

- To use this code, python needs to be installed. One possibility to do this is with [conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html). Make sure to install also the needed libraries with the correct version number.
- Then download this repository and in Terminal, cd into the main directory.
- Prepare an excel file similar to the "example_file.xlsx" containing all measurements for which z-scorees should be computed.
- __IMPORTANT__: the columns need to have the __same__ names.
- Compute the z-scores, which will be saved into the same file, by running the following command:
```run
python scientific_zscore_app.py --filename="example_file.xlsx"
```
- if the wanted excel file is not in the same directory, also the (relative or absolute) directory needs to be provided with the filename, e.g. if the file is on the desktop of user '--filename="~/Desktop/example_file.xlsx"'.
- different reference values are provided for children and adults (i.e. for different body composition parameters), therefore some of the z-scores might be empty.


## Citation
If you find this code useful or if you use it for your own work, please cite the papers referenced above.






