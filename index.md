
# Introduction

The purpose of our project is to extract valuable insights about research trends around the world and shed some light on popular technologies by analyzing granted patents throughout years. In first part of the project, we start by giving certain summary and statistics about patents according to countries and companies. We wanted analyze the evolution of granted patents over time with the purpose of extracting meaningful informations relative to various sectors. In the second part of the project, we to dive deeper in analysis and explore some of the most popular technology sectors of this century. More specifically, the sector we are interested in are energy, financial technologies and artificial intelligence. Most part of the project is structured around these three sectors. The latters were studied in order to understand their evolution in the time and reveal their relationships with belonging companies and countries.

# Dataset

The dataset used in this study is acquired from [PatentsView](http://www.patentsview.org). PatentsView provides an highly convenient API that allowed us to search for patents according to many different criteria such as to a patent title, inventor or locations. For instance, it is possible to look for how many patents in a specific topic were delivered by IBM in California from 2012 and 2015.

In addition to PatentsView dataset, various other resources were used to get certain required informations for the second part of the analysis such as [defence industry rankings](http://people.defensenews.com/top-100/)[2] Defense News  and the [list of top technology companies](http://fortune.com/2015/06/13/fortune-500-tech/)[3] from Fortune.

# Tools and Libraries

This section briefly mention about main tools and libraries used for the project. Programming language used was Python since it has all of the required libraries needed to conduct this study. Some of the libraries can be listed as follows: [Pandas](https://pandas.pydata.org) which provides high-performance, easy-to-use data structures and data analysis tools, [Matplotlib](https://matplotlib.org) which is a plotting library that can produce high quality figures in a variety of formats across platforms, [Seaborn](https://seaborn.pydata.org) which is a more advanced Python visualization library based on Matplotlib, [Beautiful](https://en.wikipedia.org/wiki/Beautiful_Soup_(HTML_parser)) Soup which is a package to for scraping and parsing HTML and XML documents and [Folium](https://folium.readthedocs.io/en/latest/#) which is a Python library to manipulate interactive [Leaflet](http://leafletjs.com) maps.

[Jupyter Notebook](http://jupyter-notebook.readthedocs.io) was used as the main development environment since it contains a highly convenient way of creating and sharing documents. This developping tool contains live code, equations, visualizations and narrative text.

# Methodology

The project can be separated into two parts. In the first part, a more general research is conducted to be able to see the overall picture of granted patents. The characteristic of granted patents was sutudied by observing their numbers through years and associate them with countries and companies. A sector-wise overview of granted patens (according to Cooperative Patent Classification categories) is provided in this study.

In the second part of the project, a deeper analysis on the most popular technology sectors in today's world is conducted. The sector of interest are grouped as energy, financial technologies and artificial intelligence. Most part of the project is structured around these three sectors. Their evolution over the time and relationship with companies/countries is reviewed in this section.

It is important to note that all the given numbers refers to granted patents approved by the USPTO (United State Patent and Trademark Office) and therefore, the statistics highlighted do not cover all patent applications around the world. However, USPTO is the most popular patent company in the word, therefor we believe our study can produce accurate results.

## 1. General Picture of Granted Patents

## 1.1. Evolution of Granted Patents in Years

In the first step, the evolution of granted patents during the last decade is displayed in order to see the general trend. The resulting line graph can be seen in the following figure.

<a id="Overview on patents growth"></a>
![Image](img/patents_overall.png)

*Figure 1: Number of Granted Patents over the last decade*

It is clear from this figure that granted patents has dramatically surged in numbers. This situation is expected since the amount of researches has also increased all over the world in 21st century.

## 1.2. Company-wise Analysis of Patents

The following figure shed the light on which companie publish most patents over the world

<a id="number_of_patents_by_companies"></a>
![Image](img/number_of_patents_by_companies.png)
*Figure 2: Number of Granted Patents Belonging to Companies*

As we can see International Business Machines Corporation (IBM) is the leading company by holding more than 120'000 patents, followed by Samsung Electronics (75'000) and Canon (65'000).

## 1.3. Country-wise Analysis of Patents

In this part, patents application classified by countries is studied. It is possible that multiple inventors are involved in a given patent. Moreover, these inventors might be located in different countries. Therefore, went through each inventors in a patent and assigned one point for a country if at least one inventor belongs to this country. It is also important to mention that for the initial analysis, we only examine the patents granted in the last year. 

<a id="last_year_patents_by_country"></a>
![Image](img/last_year_patents_by_country.png)
*Figure 3: Number of Granted Patents in the Last Year by Countries*

The following map displays the dispersion of patents applications around the world

<a id="patents_by_country"></a>
![Image](img/patents_by_country.png)
*Map 1: Map of Granted Patents in 2016*


## 1.4. Analysis of Patents belonging to Countries by CPC Categories

The Cooperative Patent Classification (CPC) is a patent categorization model which has been jointly developed by the European Patent Office (EPO) and the United States Patent and Trademark Office (USPTO).

CPC categories are indicated in the following table.


| **CODE** | **DESCRIPTION**   |
|------|------|
|   **A**  | Human Necessities|
|   **B**  | Operations and Transport|
|   **C**  | Chemistry and Metallurgy|
|   **D**  | Textiles|
|   **E**  | Fixed Constructions|
|   **F**  | Mechanical Engineering|
|   **G**  | Physics|
|   **H**  | Electricity|
|   **Y**  | Emerging Cross-Sectional Technologies|

*Table 1: Patent Categories according to Cooperative Patent Classification*

In that section, patents are studied by CPC sectors and sorted by top countries. The analysis highligh the granted patent within the last year. Resulting graphs are as follow:

![Image](img/patents_by_categories.png)
*Figure 4: Number of Granted Patents in the Last Year according to CPC Categories with Bar Charts*

Only some of the figures were drawn because of space concerns. All the figures can be reached from our [notebook](LINK REQUIRED). Almost for all of these categories United States and Japan take the 1st and 2nd place. Switzerland, South Koreas or Germany took the 3rd place according to different CPC categories. To be able to see all of these ranking in a single figure, a stacked bar chart is plotted (Figure 5).

<a id='patents_by_categories_stacked'></a>
![Image](img/patents_by_categories_stacked.png)
*Figure 5: Number of Granted Patents in the Last Year according to CPC Categories with a Stacked Chart*

To reveal more insights related to patent characteristics, spider charts were used to shed the light on which contry is focus on which sector. Below, some figures for certain countries of interest are displayed (United States, Japan, Germany and Switzerland). The rest can be obtained from our [notebook](LINK REQUIRED).

<a id='patents_by_categories_spider'></a>
![Image](img/patents_by_categories_spider.png)
*Figure 6: Number of Granted Patents in the Last Year according to CPC Categories with Spider Charts*

This figures reveal that Japan and the United States hold most of their patents in the Electricity and the Physics sectors while Switzerlands patents are more concentrated on Chemistry, Humans Necessities and Physics. Germany seems to hold significant number of patents in Transportation sector.
It is clear from these charts that Germany and Switzerland are much more polyvalent than United States and Japan since they have highly diversified patents across many of the CPC sectors.

## 2. Sector-Specific Analysis of Granted Patents

This part aims to study the evolution of granted patents by sector of interest (Energy, Fintech and AI).

To retrieve the patents from the Patentsview database, keywords and IPC symbols are used. IPC symbols allows to classify patents from different sector. For example the IPC symbol F01B 3 (F = Mechanical engineering, lighting, heating, weapon, 01 = Machines or engines in general, B = Steam engines, 3 = Reciprocating-pison machines or engines with cylender axes). Keywords allows us to confirm that the patent technology from IPC correspond exactly to what we are looking for.

In order to help us to find the IPC symbols corresponds to which sector, the website http://www.wipo.int/classifications/ipc/en/ is used. IPC symbols are searched separately to confirm they match with our sector criterium.

## 2.1 Energy Patents Analysis

Energy is a high-end sector that changed significantly over the years. The renewable energy sector became more and more unavoidable to fight against global warming. Some new technologies emerged whereas some other became less attractive. This part of the study aims to highlight the new trends in energy. Three different categories will be compared : Renewable energy, coal and gas, nuclear energy. By analyzing this sector, a study will be carried out to understand how countries are taking more consideration of global warming, trying to get rid of fossil energy or decrease their nuclear research. Inside the renewable category, many subcategories will be studied : solar photovoltaic, solar thermic, wind, hydro, wave and tidal, carbon capture and storage. All these technologies will be compare from 2006 to 2016.

The keywords used for the renewable energy technology are given in the paper "Patent-based Technology report - Alternative Energy Technology" made by the "World Intellectual Property Organization", which gives a fairly accurate result. For the nuclear/coal and gas sector, the website http://www.wipo.int/classifications/ipc/en/ is used. For the latter, keywords are researched and every potential IPC symbols are studied separately to find a match in the category.

Patentsview API is used to send queries to the database to obtain the number of patents over years for every sectors.

### Evolution of the different sectors in energy

<a id='patents_solar_photo'></a>
![Image](img/patents_solar_photo.png)

*Figure 7: Evolution of solar photovoltaic technology*

<a id='patents_solar_thermal'></a>
![Image](img/patents_solar_thermal.png)

*Figure 8: Evolution of solar thermic technology*

Even if the photovoltaic technology is more important than the solar thermic technology in term of number of patents, both sectors had a huge increase, especially during the past 4 years

<a id='patents_wind'></a>
![Image](img/patents_wind.png)

*Figure 9: Evolution of wind technology*

Wind energy has more patents than solar energy in 2007/2008. However if we sum up both solar technologies, wind and solar energy have a similar number of patents in 2016.                    

<a id='patents_hydro'></a>
![Image](img/patents_hydro.png)

*Figure 10: Evolution of hydropower technology*

Hydro does not have a large number of patents. Howerver, we could expect that this technology is outdated since dams were built many years ago (at least in Switzerland). In fact, as the other energy sectors and the number of patent in general, hydroelectric technology also evolved fast in the past.

<a id='patents_wave_and_tidal'></a>
![Image](img/patents_wave_and_tidal.png)

*Figure 11: Evolution of wave and tidal technology*

As we can observe, wave and tidal turbines were irrelevant in 2007. In the next years this technology became more important and the number of patent became hundred times greater in 10 years.

<a id='patents_carbon_capture'></a>
![Image](img/patents_carbon_capture.png)
                        
*Figure 12: Evolution of carbon capture technology*

Carbon capture almost didn't exist in 2007 but increased greatly in the past years although the number of patents is very volatile

<a id='patents_coal_and_gas'></a>
![Image](img/patents_coal_and_gas.png)

*Figure 13: Evolution of coal and gas technology*

As the other sector, fossil energy had an increase in research from 2013 to 2015. However, it decreases in 2016. We can expect the trend to contimue in that direction.

<a id='patents_nuclear'></a>
![Image](img/patents_nuclear.png)

*Figure 14: Evolution of nuclear technology*

The number of patents for nuclear energy also blew up in from 2013 to 2016. Even the nuclear catastrophe that occured in Fukushima didn't change the number of patent applications in that area.                       

### Comparison between renewable energy vs coal and gas technologies

<a id='patents_renewable_vs_coal_and_gas'></a>
![Image](img/patents_renewable_vs_coal_and_gas.png)

*Figure 15: Renewable vs coal and gas technologies*

The plot above shows clearly that there were the same number of patents between fossil energy and renewable around 2007 and 2009. After 2009 it can be note that the patent applications for renewable energy evolved much faster. In 2016, the number of patent in coal and gas decreased, we can then expect that the difference between both categories will increase even faster in the future.

### Comparison of growth in number of patents

The evolution of granted patent in energy can be compared between each other for the past 10 years. In order to achieve this pupose, the growth of patents per year was computed according to the folowing formula :

\begin{equation*}
Growth  = \frac{nb\ patents\ year\ i+1\ -\ nb\ patents\ year\ i}{nb\ patent\ year\ i}
\end{equation*}

Below, the plot showing the average growth in patent application is displayed. The black straight represents the standard deviation.

<a id='avg_growths_energy'></a>
![Image](img/avg_growths_energy.png)

*Figure 16: Average growth for the different technologies*

The bar plots above highlight the fact that solar energy is a trend nowadays. Carbon capture is a very new technology that is espected to evolve very fast in the future. However, as we can see in the table containing the number of patent, this sector does not contain many patents and the standard deviation is large. Therefore the future of this technology is uncertain. By looking at the 3 average growths on the right, it can be observed that renewable energy has evolved more in the past than fossil energy. Despite the fear of nuclear energy, the number of patents in that sector still exploded and evolved faster espessially in the past few years. However, the number of patents in renewable and fossil energy remains much larger. It is also important to note that the patents in nuclear energy might also include the research to make the technology safer.

### Correlation matrix

A study of the relation between the growth in the different sectors can be studied. For exemple, it can shown that when the hydro sector grows, the wind sector will grows as well. A correlation matrix can be computed to highlight these relations. The more the correlation is close to one, the more both sectors are growing together.

<a id='correl_matrix_energy'></a>
![Image](img/correl_matrix_energy.png)

*Figure 17: correlation matrix between the different technologies*

It can be observed that the technology in solar termic and photovoltaic evolve together. Wind and Hydro technologies seem to be highly correlated. We could suppose that those technology are complementary and that governements encorage investments in both technologies at the same time. Tidal and wave as well as carbon capture are not correlated to any other energy secors. It can be explained that those technologies are new compare to the others and therefore more volatile. It is interesting to note that carbon and gas technologies have high correlation with nuclear energy. If some countries are not focus on green energy, the investment in these 2 sectors will be fostered. With a correlation of 0.97 between the wind energy and renewable energy in general, it can be deducted that wind energy represents the general trend in green energy (This is the sector with most of the patents).

### Comparisons of renewable energy patents between companies and countries

For this next study, only the patents between 2010 and 2016 will be retreived from the database. Indeed, it takes less compilation time and shows a sufficient ammount of date for companies and countries.

<a id='word_map_renewable'></a>
![Image](img/word_map_renewable.png)

*Figure 18: patents application in renewable energy around the world*

This map shows the number of USPTO patents application around the world

The next study cassifies each technology by countries

<a id='countries_solar'></a>
![Image](img/countries_solar.png)

*Figure 19: solar energy by countries*
                        
 <a id='countries_wind_hydro'></a>
![Image](img/countries_wind_hydro.png)

*Figure 20: wind energy and hydro energy by countries*
                        
 <a id='countries_tidal_and_wave_carbon'></a>
![Image](img/countries_tidal_and_wave_carbon.png)

*Figure 21: solar energy by countries*

Every technologies are dominated by the US, especially for solar thermic, hydro, tidal and wave. This is not surprising since USPTO is a US company.

**Solar Photovoltaic**: Japan, Korea and Taiwan follows the US in the ranking. It can be note that their investment in this sector highly increased in the past 3 years. Germany, France and China arrive after in the ranking

**Solar Themic**: US and Japan are the first for this technology. However, European countries like Germany or Spain are 3rd and 4th with a big investment in that sector in 2015.

**Wind**: Germany outperforms Japan in that sector and takes the second rank. We can also note the big effort of Denmark in that area with a 4th rank. The politic of developping wind energy in those 2 European countries explains their good performance

**Hydro**: This sector is highly dominated by the US followed by Japan and Germany. Canada is ranked 4th with 62% of its energy produce by hydroelectricity.

**Tidal and Wave**: This technology is highliy dominated by the US. The UK becomes second with a high investment in 2014. We can notice that European countries like France, Spain, Italy, Norway and Finland are also investing in this technology, especially the past few years.

**Carbon Capture**: Japan and Korea are at the forefront of the research for this technology after the US and invested a lot during 2016 which is auspicious for the future.

**Renewable energy in gerneral**: The ranking follows the general trend of all the specific renewable energy with the US fist, followed by Japan, Germany, Korea and Denmark. We can note that China which is a big country is only 9th and Russie do not even appear in the top 10. (This part is only available in the notebook to not overload the website)


The next study cassifies each technology by companies

<a id='companies_solar_photo'></a>
![Image](img/companies_solar_photo.png)

*Figure 22: solar photovoltaic energy by companies*
                        
<a id='companies_solar_thermal'></a>
![Image](img/companies_solar_thermal.png)

*Figure 23: solar thermic energy by companies*

<a id='companies_wind'></a>
![Image](img/companies_wind.png)

*Figure 24: wind by companies*
                        
<a id='companies_hydro'></a>
![Image](img/companies_hydro.png)

*Figure 25: hydro by companies*

<a id='companies_tidal_and_wave'></a>
![Image](img/companies_tidal_and_wave.png)

*Figure 26: tidal and wave by companies*
                        
<a id='companies_carbon_capture'></a>
![Image](img/companies_carbon_capture.png)

*Figure 27: carbon capture by companies*

Different companies are leaders for different sectors:

**Solar Photovolataic**: SunPower Corporation is first, it is a solar panel supplier based in San Jose, CA and is a subsidiary from Total. This company is known for their highly performant solar panel. Then comes the multinational US company IBM and the Japanese company Sharp.

**Solar Thermic**: SunPower Corporation is also first for the thermic solar panel followed closely by Abengoa which is a spanish company. It confirms the fact that Spain arrives 4th in the ranking for solar termic panels.

**Wind**: The multinational US company GE active in many energy sector is the first patent company for wind. Vestas which is a danish company is 3nd. The latter is only active in wind energy and is highly responsible for the good ranking for Denmark in that area.

**Hydro**: Caterpilar dominate the market in terms of Hydro patents. Even if their main area is construction machine, they also provide equipments for hydropower plants.

**Tidal and Wave**: The market is shared by many companies in that sector and we can note that none of them are multinational but specialised in this sector. Many of them started their invesments in 2015/2016. Therefore we can conclude that this area has a big potential. The first company (Ocean Power technology) is from the US, the second (Voith) is from Germany and the third is the National Taiwan University.

**Carbon Capture**: this sector is dominated by Samsung. We can note that they provided most of the patents in the past 2 years (2015/2016). Therefore we can conclude that they are inversting a lot in that technology and are expected to grow even more in that sector. The same conclusion can be drawn for the japanese company Toshiba who started to invest in Carbon Capture in 2014.


## 2.2. FinTech Patents Analysis

Financial Technology (or FinTech) [10] is a ‘new’ financial industry that applies technology to improve financial activities . Among the several applications of FinTech we can cite a few such as new automated financial advisors, P2P lending platforms, new contactless payment technologies such (NFC, Twint, Apple Pay, etc.), blockchain application and development of cryptocurrencies (e.g. bitcoin, ethereum, etc.) personal finance applications that aim to help individuals and businesses develop a budget, and many more.

According to Google Trends, the word “FinTech” is searched 201’000 times each month on average, and this number is growing very fast in the future. Below is  a graph showing the interest over the last 6 years for FinTech.  A value of 100 is the peak popularity for the term. A value of 50 means that the term is half as popular.

<a id='google_trends'></a>
![Image](img/google_trends.png)
                        *Figure 28: Popularity of the search term “FinTech” on Google*

From our PatentsView database,  we queried the FinTech patents of the last 10 years by IPC (International Patent Classification), which is a hierarchical patent classification system. To make our research more specific, we created a set of keywords related to FinTech (financial technology, distributed ledger, cryptocurrency, trading, etc.), and filtered the outcome the IPC results accordingly.
Here is a preview of our filtered query:

<a id='ipc_head'></a>
![Image](img/ipc_head.png)
                        *Figure 29: Overview on the search by IPC*

An interesting idea would be to count the patents by year to visualize the evolution of the FinTech patents to get a clear insight into their growth over the past decade.

<a id='evolution_fintech'></a>
![Image](img/evolution_fintech.png)
                      *Figure 30: Evolution of the FinTech related patents*

This phenomenal growth indeed explains the Google growth of popularity. The FinTech domain have seen its patents grow from late 2005 all the way up to 2013 to reach a peak of 709 patents. Notice here that the number of patents almost doubled between 2009 and 2010 right after the introduction of Bitcoin, which was the start of a patent technology race for the cryptocurrency companies. We will talk about this a little further.

It is important to locate where is all this growth concentrated, therefore we took advantage of our database to collect the FinTech patents by country so we can get a clear view on the world distribution of these patents.

<a id='world_fintech'></a>
![Image](img/world_fintech.png)
                        *Figure 31: Dsitribution of FinTech Related Patents around the world*


Funny story here is that ‘Robert A. West’ holds the most patents in FinTech, what are the odds! After some googling it turned out that he was not our professor at all. As a matter of fact, Robert A. West is a intellectual property (IP) specialist who devoted his life to the creative process, and filing a large number of patents, 67 of which are FinTech related.

<a id='fintech_people'></a>
![Image](img/fintech_people.png)
                        *Figure 32: TOP 10 people issuers of FinTech patents*

Let us now talk a little bit more about who issues the most FinTech patents among the firms worldwide.

<a id='fintech_companies'></a>
![Image](img/fintech_companies.png)
                        *Figure 33: TOP 15 companies issuers of FinTech patents*

Trading Technologies International Inc. [11] is a Chicago based company that develops and delivers professional trading software platforms for trading around the world. It takes the lead of FinTech patents by issuing about 350 patents so far. Among the known companies, American Express ranks 3rd, eBay 5th, IBM 6th and VISA 11th.

We now focus on the blockchain technology. According to ‘the Economist’, blockchain is defined as a continuously growing list of records, called blocks, which are linked and secured using cryptography. Blockchain is used in a strong P2P network t0 anonymize and secure the transaction of cryptocurrencies around the globe. We scrapped the website of Clarivate Analytics [12], which is an independent company that owns and operates a collection of patents, seeking the first world issuers of blockchain patents. We came up with the following firms:

<a id='blockchain_firms_quote'></a>
![Image](img/blockchain_firms_quote.png)
    *Figure 34: Leader firms in Blockchain related patents*



## 2.3. Artificial Intelligence Patents Analysis

In this section of the project, we tried to anaylze patents related to Artificila Intelligence (AI) in a  comprehensive manner. We structered the section in the form of question and answer so, for each research question we tried to answer there is a sub-section. Before answering any questions, we gathered all the patents related to AI from 1976 until 2017 along with informations about their inventors, citations, companies and belonging countries.

The method we followed to acquire AI patents is two fold. First, we only consider IPC category "G06" which corresponds to "Computing; Calculating; Counting". According to our researches this is the main category where AI patents fall under. In addition to AI patents, this category contains many others and therefore, we only considered patent that has one of the AI related keywords in their titles. These keywords are gathered from different sources[4](https://phrasee.co/ultimate-glossary-artificial-intelligence-terms/) [5](https://business.twitter.com/en/blog/artificial-intelligence-terms-marketers-need-to-know.html) and can be accessed from [here](data/ai_keywords.txt). We consider a patent related to AI if its description contains one of these keywords. And more information related to IPC categories can be found [here](http://www.wipo.int/classifications/ipc/en/).

As we mentioned earlier, PatensView allows requesting patents only up to 100'000 at a time, to be able to gather all AI patents, we needed to request them in monthly chunks for each year. It is also worth mentioning that, it is required to clean the dataset since it was a bit messy in its raw form. Structure of the resulting dataset can be seen Table 2.3.1.

| **ID** | **Title** | **Citations** | **Country** | **Organization** | **Inventor ID** | **Inventor Name** | **Year** | **Month** |
|------|------|------|------|------|------|------|------|------|
| 4001787 | Data processor for... | 11 | US | IBM | 3959777 | Milton Jay Kimmel 	 | 1977 | 1 |
| 3942153 | Document transport... | 3 | US | Recognition Equipment Incorporated | 3942153 | Jack E. Balko | 1976 | 3 |
| 3947817 | Optical character recognition... | 50 | US | Recognition Equipment Incorporated | 3947817 | Stanley C. Requa | 1976 | 3 |
| 3967241 | Pattern recognition system | 24 | JP | Ricoh Co. Ltd. | 3967241 | Ryuichi Kawa | 1976 | 6 |
| 3967243 | Character pattern normalization... | 17 | JP | Kabushiki Kaisha Photron | 3967241 | Ryuichi Kawa | 1976 | 6 |

*Table 2.3.1: Sample Rows from the Dataset of Artificial Intelligence Related Patents*

At this point, we have the required data to be able to start answering questions. We wanted start with a basic one.

## 2.3.1. Which are the most cited patents (by other US patents) within the field of artificial Intelligence?

In our initial analysis we observe that, the patent dataset has a field for number of times that a particular patent cited by other patents however, further analysis showed that this field based only on US patents. More clearly, the description of this field is as follows: "Number of times the patent was cited by other US patents". Consequently, we don't have information about citations from other countries and decided to restrict the scope of this question into citation made only by US patents.

Note that actual patents are not only from US, just the number of citation that a particular patent have is calculated only by citation of other US patents.

| **ID** | **Title** | **Citations** | **Country** | **Organization** | **Inventor Name** | **Year** |
|------|------|------|------|------|------|------|
| 5933822 | Methods for an information retrieval... | 599 | US | Microsoft Corporation | Lisa C. Braden-Harder | 1999 |
| 6055573 | Communicating with a computer based... | 598 | US | SuperMarkets Online, Inc. | Will H. Gardenswartz | 2000 |
| 6363160 | Interface using pattern recognition and tracking | 456 | US | Intel Corporation | Boon-Lock Yeo | 2002 |  
| 6430539 | Predictive modeling of consumer financial behavior | 392 | US | HNC Software, Inc. | Ted E. Dunning | 2002 |
| 8035624 | Computer vision based touch screen | 331 | US | Intellectual Ventures I LLC | Philip L. Gleckman | 2011 |

*Table 2.3.2: Sample rows from Artificial Intelligence Patents Rankings by Citation Numbers*

Because of space concerns we only put a sample from top-cited AI patents, the whole ranking can be reached from our [notebook](LINK REQUIRED).

Looking at the names of top cited patents, they potentially, have lots of usage areas. Take for example, *"Predictive modeling of consumer financial behavior"* patent, it would clearly, be beneficial for any kind of company that interests in financial behaviour of its consumers (which is pretty much any company). Therefore, the popularity of this patent and the situation that it is being used by many other patents is highly expected. This is true for other top-cited patents in this list.

Another expected situation is that if a patent is granted earlier than others then it should have more citation and this is the case for most of the top-cited patents however we also observe that there are some patents relatively new (e.g. 2002, 2011). This might be an indication of that innovations in this area still continues and there are many researches and technologies that are benefiting from these patents.

As we mentioned, we don't have information about number of citations that a patent get by other patents apart from citations by US patents. This means that we don't have a global picture of patent citations and for this reason, we decided restrict this part of our study to only analyzing top cited patents (as we did above). Since our study is not country specific, analyzing citation data we have would only be related to US and therefore  wouldn't align with the purpose our study. Next, we move into more detailed analysis of AI patents.

## 2.3.2. How much artificial Intelligence related patents granted through years and what its the ratio of them among other patents?

Related to above question, we also hope to investigate following ideas. We know from common knowledge that AI related researches increased and decreased again during past decades, can we observe this patern by analysing the number of patents granted through years (in 1900s)? AI is also, one of the most popular area of research in today's world. Will these popularity will fade away like it did in the past or the haracteristic of the popularity trend is different this time?

To answer this question, we calculated number of AI related patents for each year from 1976 until 2016. (At the time of analysis, data for 2017 was incomplete and not taken into consideration.) The corresponding figure is as follows.

<a id='number_ai_patents_by_year'></a>
![Image](img/number_ai_patents_by_year.png)
*Figure 35: Number of Artificial Intelligence Related Patents in Years*

From this figure, it seems that there are two periods of time where number of AI patents raised that are around 1986 and 2006. Other than these periods, the amount of AI related patent seems pretty steady. But considering that overall number of patents has also increased over years, to be able to see the whole picture and make a more complete analysis, we also need to check the percentage of AI patents among all patents through years (Figure 2.3.2).

<a id='percentage_ai_patents_by_year'></a>
![Image](img/percentage_ai_patents_by_year.png)
*Figure 36: Percentage of Artificial Intelligence Related Patents in Years*

There are couple of observations worth mentioning about these figures. **First** of all, above graph starts with a decline from 1976. We already know that AI was popular field of research at 1960s (e.g. Artificial Neural Networks invented in this period.) and its popularity started to decline around 1970s (because of insufficient computing power and datasets). Although, we don't have information of patents in 1960s, we can see that the graph starts with a steady line in 1976 then, rapidly declines in 1977. It continues to fall for 3 years until it hits the lowest value in 1980.
The rate in 1977 is only reached again in 1989 which is 12 years lates.  So, the graph confirms our knowledge about the popularity of AI researches in 1960s. With this information, we believe that it is safe to assume, percentage of AI patents is an indication of popularity in AI researches. **Another** interesting point is that percentage of AI patents dramatically increases from 1987 to 1994 then, stays steady about 3 years until it starts to decline again for 5 years, until 2002. The rate of AI patents in 1996 is only reached after 10 years later, around 2006. We can see that this trend is pretty similar to 1960s', it starts with a rapid increase, followed by a steady period then, a decrease for couple of years and in both situation, around 10 years had to past before the rate came back to where it was. In light of this information, we can try to analyze the **current situation**. We see that there is a dramatic increase on patent rates from 2002 to 2012 then, it stays about the same with minor fluctuations. The characteristic that increasing rapidly and entering into steady phase is pretty similar to what we observed in last decades however it seems that the steady phase are not followed by a decline since the rate starts to increase again in 2016. Although this might be an indication that popularity of AI related researches won't decline this time, it is still too early to infer that. The first two phases were similar to what has been observed in the past decades but it requires time (at least couple more years) to decide whether this time will characteristic of the trend will be different or not.

One other valuable observation is that the AI researches are dramatically increased over 40 years, it was around *30 per/year with 0.03 percentage* and it is around *700 per/year with a percentage of 0.12* now.

As the next step, we wanted to analyse inventors.

## 2.3.3. Who are the most prolific inventors in the field of artificial intelligence?

Since we already have the required data, we just calculated number of patents that delivered by each inventors. Top inventors with highest number of patents in a sorted order can be seen in the following figure.

<a id='prolific_inventors'></a>
![Image](img/prolific_inventors.png)
*Figure 37: List of Prolific Inventors in the Field of Artificial Intelligence*

There is not much to interpret about this table (since we are already analyzing related companies and countries in other parts of the study). However, here is some information about top AI patent holders which confirms that we are on the right track.

**[Philip Yu](https://en.wikipedia.org/wiki/Philip_S._Yu)** is an American computer scientist and Professor in Information Technology at the University of Illinois at Chicago, known for his work in the field of data mining[6].

**[Dharmendra Modha](https://en.wikipedia.org/wiki/Dharmendra_Modha)** is an Indian American manager and lead researcher of the Cognitive Computing group at IBM Almaden Research Center. He is known for his pioneering works in Artificial Intelligence and Mind Simulation[7].

Now, we move into company-wise analysis of AI related patents.

## 2.3.4. Which companies are holding most artificial Intelligence related patents?

To answer this question, we grouped the dataset according to companies and sorted them by number of patents. The findings are as follows.

<a id='number_of_ai_patents_by_company'></a>
![Image](img/number_of_ai_patents_by_company.png)
*Figure 38: Companies Holding the most Artificial Intelligence Related Patens*

As expected, IBM who has the highest number of patents in all categories has also the most AI related patens. Microsoft and Google takes the second and third places which are two of the biggest technology companies that are also known for their interest in AI researches.

Although this figure reveals valuable information about companies that are highly active in AI researches, we also wanted to examine companies that devotes most of their resources into AI related researches and analyze the benefit of these researches to companies. More specifically, the question we want to answer is as follows.

## 2.3.5. Is there a relationship between investing in artificial intelligence researches and being among top companies (according to  Fortune 500 list)?

In order to find how much resources are invested in AI researches, we decided to calculate ratio of AI patents among all other patents that a company have for each company. We just calculated number of AI related patents for each company and already have the information about [overall number of patents](number_of_patents_by_companies) (from first part of our study). With these, we calculate the percentage of AI related patents  within companies (Figure 2.3.5)

One important point to note is that for some companies, it is the case that they only have couple of patents which are all related to AI so, percentage of AI patent for this company ends up being 100%. Since, we only insterested in big companies in this study, we decided to remove all the companies that has less than 1'300 patents in general. Basically, we are interested in big companies that are devoted some part of their resources into AI researches and the correlation between this investments and their ranks.

<a id='percentage_ai_patents_by_companies'></a>
![Image](img/percentage_ai_patents_by_companies.png)
*Figure 39: Ratio of Artificial Intelligence Related Patents among All Others by Companies*

This figure reveals the rankings of companies based on how much of their patents are related to AI and this intuitively means that how much of their resources devoted to AI researches.

Now, we wanted to see whether or not investing AI research would end up increasing the rank of a company. For this purpose we decided to match companies we found (by the number of AI patents) with the companies in [Fortune 500 list](http://fortune.com/2015/06/13/fortune-500-tech/)[3]. Note that within that list, we only take companies related to computer software and information systems into account since it is highly probable that only these companies made considerable amount of researches related to AI. The results are demonstrated in Figure 2.3.6.

<a id='percentage_ai_vs_fortune'></a>
![Image](img/percentage_ai_vs_fortune.png)
*Figure 40: Top Companies Invested in AI Researches and Their Presence in Fortune 500 List*

From this figure we can see that companies that invested in AI research more (which derived from proportion of AI patents they have) is more likely be in the Fortune 500 list. As the AI research proportion decrease chance of a company being among the top companies also, decreases. We can see that there is only one company in the Fortune list with less than 0.2 AI patent ratio which corresponds to rank 50 in our list (as seen in the figure). This means, all the technology companies (except one) in Fortune 500 list are from top 50 in the ranking we calculated by AI patent ratio.

For ease-of-read, here is the complete list of top AI invested companies that made it to the Fortune list (which are red dots above).

| **Organization** | **Ratio of AI Patents** |
|------|------|
| Yahoo! Inc. | 2.22 |
| Google, Inc. | 1.75 |
| Symantec Corporation | 1.69 |
| Oracle International Corporation | 0.96 |
| Facebook, Inc. | 0.87 |
| Amazon Technologies, Inc. | 0.85 |
| IBM | 0.69 |
| Xerox Corporation | 0.49 |
| NCR Corporation | 0.47 |
| Cisco Technology, Inc. | 0.41 |
| Hewlett-Packard Development Company | 0.40 |
| Nvidia Corporation | 0.25 |
| Qualcomm, Inc.| 0.22 |
| Intel Corporation | 0.18 |

*Table 2.3.3: Top Companies Invested in AI Researches and Their Presence in Fortune 500 List*

With that, the company-wise analysis is concluded and now, we can move into investigating countries.

## 2.3.6. Which countries have the most patents related to artificial intelligence?

We though that the best way to indicate the overall AI related patents that each countries while also displaying the change in number in years is use stacked bar chart (Figure 2.3.7). Note that, there is also an interactive visualization that displays number of AI related patent throughout years in our [notebook](LINK REQUIRED).

<a id='number_ai_by_countries'></a>
![Image](img/number_ai_by_countries.png)
*Figure 41: Countries that Has the Highest number of Artificial Intelligence Related Patens in Years*

From this map, it is clear that number of AI related patents has increase signiﬁcantly over years. We also, observe that United States and Japan takes the lead again and most of these countries are the ones known for their technological advancement. It is worth mentioning that although Isreal (IL) couldn't make it to the top in terms of [total number of patents](#last_year_patents_by_country), it is 5th country in AI related patents ranking. This situation is exceedingly interesting since Isreal is one of the most impactful countries in the Middle-east and AI researches might have an effect on that. We examine this idea more in the following section.

Similar to [the map we draw](#patents_by_country) in the first part of the project, we wanted draw a choropleth map to be able to see the distribution of AI related patents around the world. As before, we used logarithmic scale to assign colors to the countries. Resulting map can be seen in the following picture and we served the interactive visualization of this map in [here](html/ai_patents_by_country.html).

<a id="ai_patents_by_country"></a>
![Image](img/ai_patents_by_country.png)
*Figure 42: Dsitribution of AI Related Patents around the world*

Last question we wanted to answer is related to a recent statement made by *Putin* which is “the nation that leads in artificial intelligence will be the ruler of the world”[1].

## 2.3.7. What is the relationship between number of artificial intelligence related patents that countries have and the rank of their defence industries?

To be able to answer this question we needed a reliable ranking for countries' defense industries. We though that using [Global Defense Companies 100 list](http://people.defensenews.com/top-100/)[2] (from Defense News), to extract the revenues of defense companies along with belonging countries then, grouping these companies by countries and summing up their revenues would give us a reasonable estimation for defense industry rankings of countries. The ranking (top 10) we calculated can be seen in Table 2.3.4.

| **Country** | **Revenue (in Milions)** |
|------|------|
| US | 220693 |
| GB | 40529 |
| FR | 27931 |
| RU | 19428 |
| IT | 9832 |
| JP | 8664 |
| IL | 8615 |
| KR | 7650 |
| IN | 3682 |
| DE | 3421 |

*Table 2.3.4: Defense Industry Ranking of Countries according to Revenues retrieved from Defence News*

Our prior analysis showed that similar to company analysis, only half of countries made it to the top defence industries list. Consequently, we decided to follow the same method as before and check which countries from our top list (based number of AI patents) made it to the top defence industries list.

One other point to mention about our choice of implementation is that unlike companies, we are not going to use AI patents ratio since we observed that calculating percentages were not really descriptive in country-wise analysis. There are a lot of countries with very few patens and just a few countries with a lot of patents (as you can see in the [figure we draw](#number_ai_by_countries)) and therefore, pruning according to certain number of patents doesn't work here. We only excluded United States and Japan to be able to demonstrate rankings of other countries more clearly. Note that we already know both US and JP are on the top defence industries list.


<a id='percentage_ai_vs_defence'></a>
![Image](img/percentage_ai_vs_defence.png)
*Figure 43: Countries that have Highest number of AI Related Patents and Their Presence in Top Defence Industries List*

Again, it is obvious that countries that have more AI related patents are much more likely to be in top defence industries list. 16 out of 47 countries (in our list based on AI related patents) were also made it to the top defence industries list. Moreover, the figure reveals that 13 of these 16 countries has more than 10 patents in AI. It can also be seen that 15 out of top 20 countries in our list (based on AI related patents) were present in top defence industries list. It can also be seen from the figure, the frequency of red dots (countries in top defence industries list) increasing as the number of the AI related patents increase.

As a result, we can actually confirm that countries which are making more revenue from their companies in defense industry (meaning that countries which have better defense industries) are also the ones which have more AI related patents. So, as Putin stated, it seems that countries who invest in AI are the potential leaders of the future. However, it also seems that Putin won't be able to make it to the list ;)

| **Country** | **Number of AI Patents** |
|------|------|
| US | 4526 |
| JP | 807 |
| . | . |
| . | . |
| . | . |
| RU | 6 |

# References

[1] Vincent, J. (2017, September 4). *The Nation that Leads in AI Will be the Ruler of the World*. Retrieved from [https://www.theverge.com/2017/9/4/16251226/russia-ai-putin-rule-the-world](https://www.theverge.com/2017/9/4/16251226/russia-ai-putin-rule-the-world)

[2] Defense News. (2017, December 19). *Top 100 for 2017*. Retrieved from [http://people.defensenews.com/top-100/](http://people.defensenews.com/top-100/)

[3] Griffith, E. (2016, June 7). *The Top Technology Companies of the Fortune 500*. Retrieved from [http://fortune.com/2016/06/07/fortune-500-technology-companies/](http://fortune.com/2016/06/07/fortune-500-technology-companies/)

[4] Phrasee. (2017, December 19). *Ultimate Glossary of Artificial Intelligence Terms* [https://phrasee.co/ultimate-glossary-artificial-intelligence-terms/](https://phrasee.co/ultimate-glossary-artificial-intelligence-terms/)

[5] Kniahynyckyj, R. (2017, August 15). *Artificial Intelligence: Terms marketers need to know* [https://business.twitter.com/en/blog/artificial-intelligence-terms-marketers-need-to-know.html](https://business.twitter.com/en/blog/artificial-intelligence-terms-marketers-need-to-know.html)

[6] Wikipedia. (2017, December 19). *Philip S. Yu*. [https://en.wikipedia.org/wiki/Philip_S._Yu](https://en.wikipedia.org/wiki/Philip_S._Yu)

[7] Wikipedia. (2017, December 19). *Dharmendra Modha*. [https://en.wikipedia.org/wiki/Dharmendra_Modha](https://en.wikipedia.org/wiki/Dharmendra_Modha)

[10] Taming the Beast: A Scientific Definition of Fintech, *Patrick Schueffel*
[https://hesso.tind.io/record/1996/files/Schueffel_Tamingthebeast_2016.pdf](https://hesso.tind.io/record/1996/files/Schueffel_Tamingthebeast_2016.pdf)

[11] Trading technologies International Inc., *Bloomberg*
[https://www.bloomberg.com/research/stocks/private/snapshot.asp?privcapId=2907578](https://www.bloomberg.com/research/stocks/private/snapshot.asp?privcapId=2907578)

[12] An Overview of the Blockchain Patent Landscape, *Clarivate Analytics*
[https://clarivate.com/blog/overview-blockchain-patent-landscape/](https://clarivate.com/blog/overview-blockchain-patent-landscape/)
