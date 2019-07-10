# Airbnb

Airbnb.ipynb explores rental properties in the Boston and Seattle areas.  It is a project for the Udacity Data Scientist Nanodegree program.

## Motivation

This project explores the Airbnb public database from the perspective of an aspiring Airbnb host.  Property rental is a risky business and requires some research before investing.  The property you choose can potentially earn - or lose - a great deal of money.

## Files

The project consists of a jupyter notebook file and two folders with data in CSV form.  The folders/files are

- Boston/ - data for Boston
- Seattle/ - data for Seattle
- Airbnb.ipynb - the jupyter notebook
- README.md - this file

(This is a rather large repository and will be deleted after the project has been approved.)

## Prerequisites

To run the code, you'll need a Python 3 package manager, such as Anaconda.

## Installing

In an Anaconda command window, run the following to set up the environment:

```
conda create -n airbnb pandas matplotlib seaborn jupyter
conda activate airbnb
git clone https://github.com/PaulNWms/Airbnb.git
cd Airbnb
jupyter notebook Airbnb.ipynb
```

## Running

After the browser opens, select Cell | Run All at the menu on the jupyter page.

## Summary

The data is explored and a number of findings are made, such as optimal location, amenities, and minimum duration of stay, etc.  These results are best conveyed graphically, so please consult the notebook for specific details.

The data does not contain rental history of the properties or any information about renters.  However, with the limited data available we are still able to infer some interesting general conclusions:

- Boston is more expensive than Seattle.  (No surprise there.)
- Most properties are located close to downtown.
- But, being close to downtown does not seem to make them more popular with renters.
- Smaller properties are more popular.
- A few properties very popular, but most are not.  (Even in real estate, life is not fair...)

## Acknowledgements

* **Paul Williams** - *Initial work* - [GitHub](https://github.com/PaulNWms)

