# Apartment Rent Price Prediction (Poland)

## Project Overview  
This project builds a predictive model to estimate apartment rental prices in Poland based on property features such as size, rooms, year built, location, and amenities.  
It uses a dataset of over 8,300 listings from 2024.  

The pipeline includes:  
- Data exploration and visualization (EDA)  
- Missing value imputation (IterativeImputer, SimpleImputer)  
- Feature engineering (room size, log transforms, scaling)  
- Categorical encoding  
- Model training (Linear Regression, Decision Trees, Random Forest)  
- Hyperparameter tuning (GridSearchCV) and cross-validation  

---

## Dataset  
28 features describing each apartment:  
- **Basics**: size, rooms, floor, year built  
- **Location**: city, coordinates, distance to center  
- **Services**: distances to schools, clinics, restaurants, etc.  
- **Amenities**: balcony, elevator, parking, storage  
- **Target**: `price` (rent in PLN)  

---

## Key Insights  
- Most apartments cost between **2,000–4,000 PLN**.  
- Highest rents in **Warsaw, Kraków, Gdańsk**; lowest in **Radom, Łódź**.  
- Strong price drivers: apartment size, number of rooms, distance to city center, and amenities.  

---

## Modeling Results  
Linear Regression and Decision Trees provided moderate accuracy, while **Random Forest clearly outperformed them**.  
The tuned Random Forest model achieved the best results, with an average error of about **1,000 PLN** on the test set.  

---

## Business Takeaways  
- Size and number of rooms are the strongest predictors and should form the base of rent estimation.  
- City and location (proximity to center, services, and points of interest) strongly influence rental price.  
- Amenities such as balcony, elevator, and parking space increase rental value.  

The model can be used by:  
- **Landlords** to set fair and competitive rental prices  
- **Tenants** to evaluate if offers are reasonable  
- **Investors** to estimate profitability of rental properties  
