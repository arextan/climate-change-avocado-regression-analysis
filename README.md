# Effects of Climate Change on Avocado Yield
## Introduction
Throughout 2022 the combination of the energy crisis, Russian invasion of Ukraine, supply chain failures and climate change caused an increase in food prices and food shortages globally. Out of those factors, climate change has been and will persist to be a threat on food security. One crop worth investigating whether climate change poses and existential threat to were avocados due its following difficulty to produce yield. Avocados are difficult to grow and are not grown in all parts of the world. Even with the right environment (soil, water, and management), it is vulnerable to extreme weather and adapt poorly to high temperatures. 

## Approach
### Hypothesis
The Null Hypothesis is that avocado yield is not affected by changes in climate, while the alternative hypothesis is that avocado yield is affected by climate change. An ideal experiment would include controlling for all factors that would go into growing avocados such as altitude of farmland, soil pH, farming expertise, pests, irrigation, etc. as well as all climate change factors like extreme weather conditions, changes in precipitation, changes in various levels of greenhouse gasses, and etc.

### Variables and Data
For simplicity, average temperature change in Celsius is the variable representing climate change. Other control variables used are the average fertilizer use in tonnes and air quality variables (total methane emissions in kilotonnes and carbon dioxide density in square kilometers). The dependent variable is avocado yield measured in hectograms over hectares. Data on these variables from 1961 to 2019 in 50 countries are sourced from the United Nations Food and Agriculture Organization. The fertilizer and carbon dioxide datasets are uploaded. The remaining datasets are too large to upload so their links are: 
* Avocados: https://www.fao.org/faostat/en/#data/QCL 
* Temperature Change: https://www.fao.org/faostat/en/#data/ET 
* Methane Emissions: https://www.fao.org/faostat/en/#data/GT

## Analysis
### Exploratory Data Analysis

![image13](https://user-images.githubusercontent.com/105828433/208839783-47c664e2-774d-4639-a4f8-09572d7c14af.gif)
![image16](https://user-images.githubusercontent.com/105828433/208839377-bf6a30dc-b95c-48a0-8721-07ed6aa67c33.gif)

Total Global Avocado Yield vs. Global Temperature Change
![image18](https://user-images.githubusercontent.com/105828433/208839926-d21e47cf-2aa1-4e2c-a850-5201585a4b75.png)

For the initial exploratory analysis, the data obtained were right skewed. For example, the right skew in avocado yield by country demonstrates that only a few countries have produced more than two hundred thousand hectograms per hectare of avocado yield per year since the 1960s. This meant only a few countries would be identified as a top producing country. This right skew phenomenon can also be seen in the methane, fertilizer, and carbon dioxide data. By log transforming these data, the data illustrated a better correlation matrix.

### Regression
Running a regression showed that variables we have chosen are significant as all of your p-values were below 5%. However, with a low R-squared value of 8.4%, only 8.4% of the variability can be accounted for with all of these variables. This led to the second regression done in this project involving countries as our dummy variable. By splitting the data per country and regressing per country, we can gain further insights on our regression such as how R-squared values are different for every country, whether a country’s yield is positively or negatively with temperature change, or whether temperature change is statistically significant on a country’s avocado yield or not.
By looking into countries with higher R-squared values (e.g. New Zealand adjusted R. Squared of 89%), this shows that most of its variability could be explained by our model and that our model is good for New Zealand. After selecting the top ten countries that returned high R-squared and the p-value of less than five percent, a list of top 10 countries whose avocado yield can be predicted well by temperature change. By summing yield from the 1960s for each country, we produced a list of top ten avocado yielding countries. We found that 3 of the countries (Cuba, Mexico & Morocco) found in this list were also in our initial list of 10 countries with high R-squared and low p-value. This means we are able to predict avocado yield for these countries using temperature. 

## Conclusion
To conclude, we can reject the null hypothesis that climate change does not have an effect on avocado yield. However, some countries are relatively easier to predict than others in terms of how temperature changes affect avocado yield. This experiment is specially useful for companies which need avocados for their raw materials, with this they will be able to predict where to get a stable and sufficient supply of avocados. We found our model works particularly well for countries that lie on the border of the tropic of Cancer and Capricorn. Within our select countries, Cuba, Mexico, and Morocco are the three main countries to source avocados from due to their more stable climate year-round that allows better predictability in terms of avocado yield. With that said, it is important to know that the findings are limited to the factors that were investigated. There are other factors mentioned in the beginning that contribute to the production of avocados as well as other factors that account for climate change such as air quality, soil pH, etc. which are not examined and should be accounted for when considering how climate change affects overall avocado yield. Furthermore, there are limitations within our data in terms of recency as it only dates back to the 1960s. Lastly, demand and population should be factored in via having the year as a control variable to ensure that the increase in yield was not due to the rise in popularity of the crop rather due to the sole factor of change in temperature.
