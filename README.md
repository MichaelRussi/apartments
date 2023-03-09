# apartments
Web scraping of apartments for sale in Itajaí, Brazil
This R code is a loop that scrapes data from a real estate website called Zap Imóveis. 
The loop iterates over page numbers from 1 to 225 and for each page, it performs the following steps:

1)Constructs a URL for the given page number using the paste0() function. The URL includes filters for location, transaction type, property type, and other criteria.

2)Uses the read_html() function from the rvest package to fetch the HTML code of the page at the constructed URL.

3)Uses the html_nodes() function from the rvest package to extract specific elements from the HTML code. Specifically, the code extracts the following information from each page:

/address: the address of the property
/square_meters: the area of the property in square meters
/bedrooms: the number of bedrooms in the property
/bathrooms: the number of bathrooms in the property
/garage: the number of parking spaces available with the property
/observation: a short description of the property
/condominium: the monthly condominium fee (if applicable)
/tax: the annual property tax (if applicable)
/price: the asking price of the property

4)Uses the rbind() function to combine the extracted data from each page into a single data frame called apartments.

5)Prints the current page number.

Overall, the code is scraping real estate data from Zap Imóveis and storing it in a data frame for further analysis or modeling.
