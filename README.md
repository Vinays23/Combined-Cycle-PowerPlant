# Combine Cycle Power Plant
A combined cycle power plant (CCPP) is composed of gas turbines (GT), steam turbines (ST) and heat recovery steam generators. In a CCPP, the electricity is generated by gas and steam turbines, which are combined in one cycle, and is transferred from one turbine to another. So with the help of Python tools and some Machine Learning algorithms, we try to predict the electrical energy.

## Install
This project requires Python 3.6 and the following libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)

You will also need to have software installed to run and execute a [Jupyter Notebook](http://ipython.org/notebook.html)

If you do not have Python installed yet, it is highly recommended that you install the [Anaconda](http://continuum.io/downloads) distribution of Python, which already has the above packages and more included.


## Run
In a terminal or command window, navigate to the top-level project directory and run one of the following commands:
```
jupyter notebook Combined Cycle Power Plant using all features with sklearn.ipynb
```
This will open the Jupyter Notebook software and project file in your browser.

## Dataset Information
The dataset contains 9568 data points collected from a Combined Cycle Power Plant over 6 years (2006-2011), when the power plant was set to work with full load. Features consist of hourly average ambient variables Temperature (T), Ambient Pressure (AP), Relative Humidity (RH) and Exhaust Vacuum (V) to predict the net hourly electrical energy output (PE) of the plant.
A combined cycle power plant (CCPP) is composed of gas turbines (GT), steam turbines (ST) and heat recovery steam generators. In a CCPP, the electricity is generated by gas and steam turbines, which are combined in one cycle, and is transferred from one turbine to another. While the Vacuum is colected from and has effect on the Steam Turbine, he other three of the ambient variables effect the GT performance.
For comparability with our baseline studies, and to allow 5x2 fold statistical tests be carried out, we provide the data shuffled five times. For each shuffling 2-fold CV is carried out and the resulting 10 measurements are used for statistical testing. 

## Attribute information
Features consist of hourly average ambient variables 
- Temperature (T) in the range 1.81°C and 37.11°C,
- Ambient Pressure (AP) in the range 992.89-1033.30 milibar,
- Relative Humidity (RH) in the range 25.56% to 100.16%
- Exhaust Vacuum (V) in teh range 25.36-81.56 cm Hg
- Net hourly electrical energy output (EP) 420.26-495.76 MW


## Output variable (desired target):
- Electrical Energy Output(PE)

## Models trained On:
| Trained Model | Root Mean Squared Error |
| --- | --- |
| Univariate Linear Regression | 0.05166 |
| Univariate Linear Regression using sklearn | 0.06982 |
| Multivariate Linear Regression [2 features] | 0.04688 |
| Multivariate Linear Regression [2 features] using sklearn | 0.06466 |
| Multivariate Linear Regression [3 features] | 0.04569 |
| Multivariate Linear Regression [3 features] using sklearn | 0.06531 |
| Multivariate Linear Regression [4 features] | 0.04107 |
| Multivariate Linear Regression [4 features] using sklearn | 0.06234 |
