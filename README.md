# Tour Itinerary Scraper from Hanatour website

I created this to help out with the internal operations during my time in HT Hoju.<br>
It was quickly created for a very specific purpose. 


## Set Up
1. Install Insomnia.
2. Then go to any of Hanatour.com website and go into any itinerary.
3. Copy the address
4. Put it in Insomnia to generate cookie details to put in the header in the 4th cell. (Might need to do some research on how to do this. It's a post request and inspect Hanatour page's API for further info as the site may change.)

## How to use it
I've designed it so that it works on google colab for it to be used by everyone in the office without having me to set up their computers individually and also that I can implement any changes quickly. <br>

Firstly, run the first cell to install the necessary packages.<br>
Then, enter the tour code (eg. PAP221231107KEY) and then enter the regions you want the itinerary for in Korean. <br>
So for example, if the tour goes to Gold Coast and Sydney but you only want the itinerary for Sydney one, you would only enter Sydney. If both: Sydney,GoldCoast. In Korean it is 시드니,골드코스트<br>
Then when you run all the cells, excel files with itineraries will be automatically downloaded. You may need to allow multiple files to be downaloded at once.<br>
I have uploaded an example of the itinerary files for reference. Please note that the primary language is Korean, as the company is predominantly, if not entirely, composed of Korean speakers.
<br>

## Further details on how to use it
This file is specifically designed for this particular office. So, the regions are very restricted to the ones stated in the function aggregate_region. <br>
What this function does is that it maps many different regions into a single region. <br>
The reason for this is because this office creates these different versions of these itinerary plans for different cities such as Sydney, Gold Coast, Brisbane, Cairns, etc as there are different people handling these people on each of the cities. <br>
There are many names of regions within each of these cities. This function maps the multiple regions to the related cities so that I can easily filter the itinerary to create one for each of the different cities. <br>
If one want to map a region to a city, simple go: <br>
{"some_region":"some_city"}
So if one requires other regions, simply add to or modify this section. <br>
<br>
Also, from time to time, one may want to renew the cookie details in the 4th cell by going into INSOMNIA and repeating the process stated above. <br>
I've not had any issues of the website blocking me but you'd never know. 
