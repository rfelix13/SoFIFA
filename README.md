# SoFIFA Player Data

A project to write a script to download all current player data from EA Sports' FIFA video game using the SoFIFA.com site, then reverse engineer the Overall rating given to each player. 

Shoutout to <a href='https://github.com/DiogoDantas'>DiogoDantas</a> and <a href="https://github.com/arnaldog12">arnaldog12</a> for their project linked <a href='https://github.com/DiogoDantas/SoFIFA'>here</a>, I did mine a bit differently but got a bit of inspiration from these guys!

Contents: 

1. Scrapy URL Spider - This notebook allows you to scrape all of the player page URLs from SoFIFA.com

2. Scrapy Stats Spider - This notebook allows you to scrape all of the player data from SoFIFA.com, and relies on the sofi_urls.jl file in the data folder that the previous notebook generates.

3. Parse Derivation - This is the notebook that I used to extract all the player data from SoFIFA in chunks and then copy the code to the parse method definition in the Scrapy Stats Spider notebook

4. Reverse Engineering Overall Ratings - This notebook uses the data in sofi_stats.jl in the data folder that was generated from the Scrapy Stats Spider notebook, and attempts to reverse engineer the overall rating system.  


### Bugs/Other Features

* Country and Club are switched for some players
* Will want to check release clause and contract details for players
* Include player image urls in scraping
* Find a way to code in the process of verifying only current player data is downloaded
* Create a DataFrame that compares the overall rating with the predictions from each model