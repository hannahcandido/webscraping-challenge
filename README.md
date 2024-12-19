Methodology
Web scraping was employed to collect the Mars temperature data from the provided URL. BeautifulSoup was used to scrape the data from the webpage, which contains an HTML table with columns representing temperature and atmospheric pressure data collected over a period of time.
The webpage was inspected to identify the table content and the relevant data. The columns of interest included:
•	id: The identification number of a single transmission from the Curiosity rover.
•	terrestrial_date: The date on Earth.
•	sol: The number of elapsed sols (Martian days) since Curiosity landed on Mars.
•	ls: The solar longitude.
•	month: The Martian month.
•	min_temp: The minimum temperature, in Celsius, of a single Martian day.
•	pressure: The atmospheric pressure at Curiosity's location.
A BeautifulSoup object was created to parse the HTML content from the webpage. The find_all method was then used to extract all rows from the table.
After scraping the data, a Pandas DataFrame was created with the same column headings as the original table on the website, providing a structured way to store and analyze the data.
The terrestrial_date column was converted into the datetime format, and the sol and min_temp columns were cast into integers and floats, respectively, ensuring the data was clean and ready for analysis.
The following analyses and visualizations were performed to answer key questions regarding Martian weather patterns:
•	How many months exist on Mars?
•	How many Martian (and not Earth) days worth of data exist in the scraped dataset?
•	What are the coldest and the warmest months on Mars (at the location of Curiosity)? 
o	The average minimum daily temperature for all of the months was calculated.
o	The results were plotted as a bar chart.
•	Which months have the lowest and the highest atmospheric pressure on Mars? 
o	The average daily atmospheric pressure for all months was calculated.
o	The results were plotted as a bar chart.
•	How many terrestrial (Earth) days exist in a Martian year? 
o	The number of days that elapse on Earth in the time that Mars completes one orbit around the Sun was considered.
o	The result was visually estimated by plotting the daily minimum temperature of each observation.
Finally, the cleaned data was exported into a CSV file for further use or analysis.
Conclusion
Following this methodology, the Mars temperature dataset was successfully scraped, cleaned, and analyzed. The analysis provided valuable insights into the Martian temperature trends, atmospheric pressure variations, and the length of a Martian year in Earth days.
