# Patent Applications Analysis

# Introduction

The idea behind our project is extracting meaningful and valuable insights about research trends around the world and shed some light on technologies related to certain sectors by analyzing granted patents throughout years. In first part of the project, we start by giving some summary and statistics about patents by countries and companies. We wanted analyze the evolution of granted patents over time with the purpose of extracting meaningful informations relative to different sectors. In the second part of the project, we are aiming to dive deeper in analysis and explore some of the most popular technology related sectors in this century. More specifically, the sector we are interested in are energy, financial technologies and artificial intelligence.
Most part of the project is structured around these three sectors. We study them comprehensively in order to understand their evolution in the time and relations with companies and countries.

# Dataset

The dataset that we used in this study is acquired from (PatentsView)[http://www.patentsview.org]. PatentsView provides an highly convenient API that allowed us to search for patents according to many different criteria such as to a patent title, inventor or locations. For instance, it is possible to look for how many patents in a specific topic were delivered by IBM in California from 2012 and 2015.

Here is a query example that returns the patent_number for patens granted after 2007.
(http://www.patentsview.org/api/patents/query?q={"_gte":{"patent_date":"2007-01-04"}}&f=["patent_number"])[http://www.patentsview.org/api/patents/query?q={"_gte":{"patent_date":"2007-01-04"}}&f=["patent_number"]]_ 

In addition to PatentsView dataset, we used various other resources to get certain required informations for the second part of our analysis such as university rankings from (Times Higher Education)[], defence industry rankings from (Defense News)[] and the list of top technology companies from (Fortune)[]...

# Methodology

The project can be separated into two parts. In the first part, we conducted a more general research to be able to see the overall picture related to granted patents. We tried to analyze the characteristic of granted patents by observing number of patent through years and associating them with countries and companies. We also give a generic sector-wise overview of granted patens (according to Cooperative Patent Classification categories).

In the second part of the project, we aimed to dive deeper into analysis and explore some of the most popular technology sectors in today's world. The sector we examined can grouped as energy, financial technologies and artificial intelligence. Most part of the project is structured around these three sectors. We study them comprehensively in order to understand their evolution in the time and relationship with companies and countries.

It is important to note that all the given numbers refers to granted patents approved by the USPTO (United State Patent and Trademark Office) and therefore, the statistics highlighted do not cover all patent applications around the world, but since USPTO is the most popular patent company, we believe that our study can produce accurate results.

## General Picture of Granted Patents

The research ideas that we investigated in this section can be listed as follows.

1. Evolution of granted patent throughout years
2. Number of granted patents by countries and companies
3. Analysis of top countries delivering patents according to CPC categories
