## 2.1. Analysis of Patents related to Artificial Intelligence

In this section of the project, we tried to anaylze patents related to Artificila Intelligence (AI) in a  comprehensive manner. We structered the section in the form of question and answer so, for each research question we tried to answer there is a sub-section. Before answering any questions, we gathered all the patents related to AI from 1976 until 2017 along with informations about their inventors, citations, companies and belonging countries.

The method we followed to acquire AI patents is two fold. First, we only consider IPC category "G06" which corresponds to "Computing; Calculating; Counting". According to our researches this is the main category where AI patents fall under. In addition to AI patents, this category contains many others and therefore, we only considered patent that has one of the AI related keywords in their titles. These keywords are gathered from different sources[1](https://phrasee.co/ultimate-glossary-artificial-intelligence-terms/) [2](https://business.twitter.com/en/blog/artificial-intelligence-terms-marketers-need-to-know.html) and can be accessed from [here](data/ai_keywords.txt). We consider a patent related to AI if its description contains one of these keywords. And more information related to IPC categories can be found [here](http://www.wipo.int/classifications/ipc/en/).

As we mentioned earlier, PatensView allows requesting patents only up to 100'000 at a time, to be able to gather all AI patents, we needed to request them in monthly chunks for each year. It is also worth mentioning that, it is required to clean the dataset since it was a bit messy in its raw form. Structure of the resulting dataset can be seen Table 2.1.

| **ID** | **Title** | **Citations** | **Country** | **Organization** | **Inventor ID** | **Inventor Name** | **Year** | **Month** |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 4001787 | Data processor for... | 11 | US | IBM | 3959777 | Milton Jay Kimmel 	 | 1977 | 1 |
| 3942153 | Document transport... | 3 | US | Recognition Equipment Incorporated | 3942153 | Jack E. Balko | 1976 | 3 |
| 3947817 | Optical character recognition... | 50 | US | Recognition Equipment Incorporated | 3947817 | Stanley C. Requa | 1976 | 3 |
| 3967241 | Pattern recognition system | 24 | JP | Ricoh Co. Ltd. | 3967241 | Ryuichi Kawa | 1976 | 6 |
| 3967243 | Character pattern normalization... | 17 | JP | Kabushiki Kaisha Photron | 3967241 | Ryuichi Kawa | 1976 | 6 |

*Table 2.1: Sample Rows from the Dataset of Artificial Intelligence Related Patents*

At this point, we have the required data to be able to start answering questions. We wanted start with a basic one.

## 2.1.1. Which are the most cited patents (by other US patents) within the field of Artificial Intelligence?

In our initial analysis we observe that, the patent dataset has a field for number of times that a particular patent cited by other patents however, further analysis showed that this field based only on US patents. More clearly, the description of this field is as follows: "Number of times the patent was cited by other US patents". Consequently, we don't have information about citations from other countries and decided to restrict the scope of this question into citation made only by US patents.

Note that actual patents are not only from US, just the number of citation that a particular patent have is calculated only by citation of other US patents.

| **ID** | **Title** | **Citations** | **Country** | **Organization** | **Inventor Name** | **Year** |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 5933822 | Methods for an information retrieval... | 599 | US | Microsoft Corporation | Lisa C. Braden-Harder | 1999 |
| 6055573 | Communicating with a computer based... | 598 | US | SuperMarkets Online, Inc. | Will H. Gardenswartz | 2000 |
| 6363160 | Interface using pattern recognition and tracking | 456 | US | Intel Corporation | Boon-Lock Yeo | 2002 |  
| 6430539 | Predictive modeling of consumer financial behavior | 392 | US | HNC Software, Inc. | Ted E. Dunning | 2002 |
| 8035624 | Computer vision based touch screen | 331 | US | Intellectual Ventures I LLC | Philip L. Gleckman | 2011 |

*Table 2.1: Sample rows from Artificial Intelligence Patents Rankings by Citation Numbers*

Because of space concerns we only put a sample from top-cited AI patents, the whole ranking can be reached from our [notebook](LINK REQUIRED).

Looking at the names of top cited patents, they potentially, have lots of usage areas. Take for example, *"Predictive modeling of consumer financial behavior"* patent, it would clearly, be beneficial for any kind of company that interests in financial behaviour of its consumers (which is pretty much any company). Therefore, the popularity of this patent and the situation that it is being used by many other patents is highly expected. This is true for other top-cited patents in this list.

Another expected situation is that if a patent is granted earlier than others then it should have more citation and this is the case for most of the top-cited patents however we also observe that there are some patents relatively new (e.g. 2002, 2011). This might be an indication of that innovations in this area still continues and there are many researches and technologies that are benefiting from these patents.

As we mentioned, we don't have information about number of citations that a patent get by other patents apart from citations by US patents. This means that we don't have a global picture of patent citations and for this reason, we decided restrict this part of our study to only analyzing top cited patents (as we did above). Since our study is not country specific, analyzing citation data we have would only be related to US and therefore  wouldn't align with the purpose our study. Next, we move into more detailed analysis of AI patents.

## 2.1.2. How much AI related patents granted through years and what its the ratio among other patents?

Related to above question, we also hope to investigate following ideas. We know from common knowledge that AI related researches increased and decreased again during past decades, can we observe this patern by analysing the number of patents granted through years (in 1900s)? AI is also, one of the most popular area of research in today's world. Will these popularity will fade away like it did in the past or the haracteristic of the popularity trend is different this time?

To answer this question, we calculated number of AI related patents for each year from 1976 until 2016. (At the time of analysis, data for 2017 was incomplete and not taken into consideration.) The corresponding figure is as follows.

<a id='number_ai_patents_by_year'></a>
![Image](img/number_ai_patents_by_year.png)
*Figure 2.1: Number of Artificial Intelligence Related Patents in Years*

From this figure, it seems that there are two periods of time where number of AI patents raised that are around 1986 and 2006. Other than these periods, the amount of AI related patent seems pretty steady. But considering that overall number of patents has also increased over years, to be able to see the whole picture and make a more complete analysis, we also need to check the percentage of AI patents among all patents through years (Figure 2.2).

<a id='percentage_ai_patents_by_year'></a>
![Image](img/percentage_ai_patents_by_year.png)
*Figure 2.1: Percentage of Artificial Intelligence Related Patents in Years*

There are couple of observations worth mentioning about these figures. **First** of all, above graph starts with a decline from 1976. We already know that AI was popular field of research at 1960s (e.g. Artificial Neural Networks invented in this period.) and its popularity started to decline around 1970s (because of insufficient computing power and datasets). Although, we don't have information of patents in 1960s, we can see that the graph starts with a steady line in 1976 then, rapidly declines in 1977. It continues to fall for 3 years until it hits the lowest value in 1980.
The rate in 1977 is only reached again in 1989 which is 12 years lates.  So, the graph confirms our knowledge about the popularity of AI researches in 1960s. With this information, we believe that it is safe to assume, percentage of AI patents is an indication of popularity in AI researches. **Another** interesting point is that percentage of AI patents dramatically increases from 1987 to 1994 then, stays steady about 3 years until it starts to decline again for 5 years, until 2002. The rate of AI patents in 1996 is only reached after 10 years later, around 2006. We can see that this trend is pretty similar to 1960s', it starts with a rapid increase, followed by a steady period then, a decrease for couple of years and in both situation, around 10 years had to past before the rate came back to where it was. In light of this information, we can try to analyze the **current situation**. We see that there is a dramatic increase on patent rates from 2002 to 2012 then, it stays about the same with minor fluctuations. The characteristic that increasing rapidly and entering into steady phase is pretty similar to what we observed in last decades however it seems that the steady phase are not followed by a decline since the rate starts to increase again in 2016. Although this might be an indication that popularity of AI related researches won't decline this time, it is still too early to infer that. The first two phases were similar to what has been observed in the past decades but it requires time (at least couple more years) to decide whether this time will characteristic of the trend will be different or not.

One other valuable observation is that the AI researches are dramatically increased over 40 years, it was around *30 per/year with 0.03 percentage* and it is around *700 per/year with a percentage of 0.12* now.

As the next step, we wanted to analyse inventors.

## 2.1.3. Who are the most prolific inventors?

Since we already have the required data, we just calculated number of patents that delivered by each inventors. Top inventors with highest number of patents in a sorted order can be seen in the following figure.

<a id='most_prolific_inventors'></a>
![Image](img/most_prolific_inventors.png)
*Figure 2.1: List of Prolific Inventors in the Field of Artificial Intelligence*

There is not much to interpret about this table (since we are already analyzing related companies and countries in other parts of the study). However, here is some information about top AI patent holders which confirms that we are on the right track.

**[Philip Yu](https://en.wikipedia.org/wiki/Philip_S._Yu)** is an American computer scientist and Professor in Information Technology at the University of Illinois at Chicago, known for his work in the field of data mining.

**[Dharmendra Modha](https://en.wikipedia.org/wiki/Dharmendra_Modha3)** is an Indian American manager and lead researcher of the Cognitive Computing group at IBM Almaden Research Center. He is known for his pioneering works in Artificial Intelligence and Mind Simulation.

With that, we move into company-wise analysis of AI related patents.

## 2.1.4. Which companies are holding most AI patents?
