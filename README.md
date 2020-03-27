## Are-the-salaries-in-the-US-better-
We are Yash and Guillermo and we are foreign students. Since we are close to graduation of our masters we are in the process of getting a job. In the US, we have learned that getting a $100,000/year job is somewhat likely to get with our degree. We also know that we would never get such salary in India and Mexico respectively (our home country). However, the question we are solving today is, given the difference in Cost of Living, what salary would we need to find in our home country that can give us the same life quality than earning $100,000/year in the US.

We have made an Excel that will allow us to do this, however it is designed so that you can make your own comparisons, put the city where you got an offer from and then compare in the dashboards with the cities and/or countries available to find the equivalent salary.

# How will we compare the salaries
We have found a Cost Of Living Index (CoL) created by expatistan. This website had a similar problem, in their case they wanted to help expats figure out if the salary they were offered in the new city was worth it. They have information of over 2000 cities in the world. However we had access to the top 260 cities. They have compared the cost of living by considering bank historical analysis as well as information provided by users. This costs consider meals, groceries, rent, social hanging outs such as movies, dinners with friends, and activities in the city. 
### How to read the CoL
    Expats have made Prague, Czech Republic as the reference city, and their index is 100.
    The index for another city is how much more expensive (or cheaper) it is to Prague. 
    For example, Baltimore's index is 160, therefore baltimore is 60% (160-100) more expensive than Prague.
    Queretaro, Mexico's index is 82% therefore living in Queretaro (82-100) is 18% cheaper than Prague. 
    In our Excel we have made adjustments so that it converts this index to monetary value which will be explained further.
    Contrary to expats, we will also include the tax deductions (since this is not considered in their analysis).
    
 # Calculation for Equivalent Salary
  Equivalent Salary is the salary (with taxes) that we would need in another city to match the salary in the city we get an offer from. 
  Note that we run this calculation to all cities, which we will then see in a Dashboard to compare multiple cities in a single view.

  ## The formula is the following:
    Equivalent Salary =  Salary offered * (1 - tax bracket in target city) * Index ratio / (1 - tax bracket in offer City)
    
      Salary offered= Net Salary offered
      Offer City = City where we get the offer from
      Target city = City we wish to compare, and obtain equivalent salary from
      Tax bracket = Federal taxes deducted from salary
      
      *It was important to divide by (1 - tax bracket in offer City) to convert back to Net Salary since our job offers are typically   shown as Net salaries rather than gross.
      
# Steps to use the Excel dashboard
  1. Go to 'Offer Review' and select the city from the list available and type the salary offered. If the city is unavailable you will get notified by the program.
      Note: The salary units are not specified, therefore consider that such unit will remain throughout. In our case the units are USD/year. If you wish to use monthly salary in another currency, consider all values in the dashboard will use such units as well.
  2. Go to 'Dashboards' and refresh both dashboards.
  3. Click in the slicers the Regions and Countries you wish to keep accordingly. 
      Note: You may need to reset filter
  4. Make conclusions.... the question you want to answer is "Can I get obtain the salary suggested with my current resume?"
  5. Try different offers, try different cities at your leasure!
  
  *For our example we will assume we got an offer of $100,000 USD/year in Baltimore.
 
 
### Yash's example
 Yash comes from Mumbai, India. In summer he looks for a full time job and finds an offer of $100,000 in Baltimore.
 He would prefer to stay in Mumbai to be with his family, therefore he want to see what salary would he need to find in Mumbai or other cities in India.
 Afther refreshing the dashboard he gets the final results:

In Mumbai he would need to get a salary of $45,000 USD/year that is $34,31,248.46 rupees a year.
After doing research and knowing the salaries in India, he believes he can find that salary in Mumbai therefore he would rather move back to India and be with his family.
<img src= https://github.com/GuillermoAlcocerDelano/Are-the-salaries-in-the-US-better-/blob/master/IndiaDashboard.png> 
 
 ### Guillermo's example
 Guillermo comes from Queretaro, Mexico. He would only move to the US if he can get a much higher salary in the US than in Mexico.
 He is engaged, but his fiancee could not work in the US because of migration status. Therefore his salary in Baltimore would need
 to offset that 'loss' the couple would have. He gets the final results:
 
 <img src= https://github.com/GuillermoAlcocerDelano/Are-the-salaries-in-the-US-better-/blob/master/MexicoDashboard.png>
 
 The equivalent salary is nearly $50,000 USD a year. In his research he believes he would not be able to get a salary greater than 
 $39,000 USD in Queretaro nor Mexico (his preferred cities). 
 However, given his fiance's new business expects to provide her $15,000 USD/year they have decided its not worth moving to Baltimore.
 
 
 
  
# Methodology
  1. Extract cost of living index per city fomr expatistant.
  2. Data cleansing
      - Split City and Country to seprate cells
      - Turn Index into a percentage by formula
 3. Collect tax bracket information of each country
      - Retrieved federal taxes for income in each country from https://tradingeconomics.com/country-list/personal-income-tax-rate
      - Use VLOOKUP to extract values to our data set
 4. Add new column called "Region" to be able to classifiy countries by their region.
      - This can be changed in sheet 'Regions per Country' which is a hidden sheet
 5. Create sheet 'Offer Review' to submit the offer to compare
     - Create rules to assure that the calculations run correctly
          - Only accept Available cities
          - Only accept numerical values in Salary
 6. Hide sheets of internal calculations
 
          
 5. Create dashboards in a separate Excel sheet.
      - Add slicers for Countries and Regions.
      
# Conclusion
 While the salaries in the US are significant higher than those in India and Mexico, so is the cost of living. 
 It is important to consider the cost of living to see if the increase in the salary makes it worh it to stay in the US.
 It is clear that every person will have their own criteria and factors to consider to move from one country to another. With this
 file we provide them with a tool to compare the salaries in an fair comparison by adjusting according to the costs and taxes
 from each city/country.
 Yash and Guillermo have decided to move back to their countries since they consider they will be able to have a similar lifestyle in
 their cities despite the total salary being much lower (even less than half the salary in the US).
    
## Sources
https://www.expatistan.com/es/costo-de-vida/indice
https://tradingeconomics.com/country-list/personal-income-tax-rate

