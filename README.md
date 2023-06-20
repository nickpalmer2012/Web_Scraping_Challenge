# Web_Scraping_Challenge
Module 11 Challenge repo
### Extracting article titles and previews and storing them into a dictionary:
 - for this I referenced the "news_solution" class activity to see the structure of the for loop used to extract, create dictionary pairs, and then add dictionaries to a blank list.
 - ![image](https://github.com/nickpalmer2012/Web_Scraping_Challenge/assets/128104435/be31ffc9-7488-49d8-99a8-abac594f944f)

### Extracting tabular data from a webpage and converting the results to a pandas DataFrame:
- I utilized chat GPT to help me construct a nested for loop in order to create a list of lists(rows) to eventually convert into a pandas DF.
- Here is the question I posed to ChatGPT: ![image](https://github.com/nickpalmer2012/Web_Scraping_Challenge/assets/128104435/59dc462b-7cab-49fd-a1a3-7ec309d7dc49)
- Excluding the imports, here is what chat GPT gave me as a possible solution:
- ![image](https://github.com/nickpalmer2012/Web_Scraping_Challenge/assets/128104435/5390ac68-a17a-4559-ba20-a43c174d55c1)

### Estimating the number of Earth days in a Martian year:
- Chat GPT wanted me to use the .apply function to apply a function to the terrestrial_date column
- This is the example code it gave me to add a column with the number of earth days that 'Curiosity' has been on Mars: df['days_since_reference'] = df['date_column'].apply(lambda x: (x - reference_date).days)

- This is my code I used to get the earth_days column:  mars_df['earth_days'] = mars_df['terrestrial_date'].apply(lambda x: (x - earliest_terrestrial_date).days)

- My understanding is that the .apply() function applies whatever function is contained within the parenthesis.
- The 'lambda x' function in this instance assigns x to the value in the terrestrial date column.
- We defined the 'lambda x' function as x minus the earliest date in the dataset.
- The result is a new column 'earth_days' in the mars_df dataframe where we subtract the first date in the dataset from the date in whatever row is being evaluated.
- We now have an xaxis to plot the min temperatures on to make a visual estimate about the length of a Martian year.
   
