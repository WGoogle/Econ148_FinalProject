# Econ148_FinalProject

Econ 148 Final Project, GDP Nowcasting from Mixed-Frequency Indicators.

## Reproducibility

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/WGoogle/Econ148_FinalProject/main)

Click the badge to launch the whole project in Binder, THIS IS OUR REPRODUCIBILITY LINK APPROVED BY PROFESSOR

Recommended run order:
1. `1_Data_Collection.ipynb`
2. `2_Baseline_Bridge.ipynb`
3. `3_MLStuff.ipynb`
4. `4_Comparisons.ipynb`

Fair warning, Binder may take a bit to run the first time. It doesn't mean its broken, just building the environment. 
Also, keep in mind that for the sake of reproduciblity, we auto saved the datasets we used in the repo. If you want to make your own API Call -- make a "secret_key.env" file and paste in FRED_API_KEY=your_api_key_here and of course replace the your_api_key_here with your actual API Key. This will allow you to then run our notebooks with your own API Call. 
