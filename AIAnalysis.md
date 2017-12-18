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

*Table 2.1: Patent Categories according to Cooperative Patent Classification*

At this point, we have the required data to be able to start answering questions. We wanted start with a basic one.

## 2.1.1. Which are the most cited patents (by other US patents) within the field of Artificial Intelligence?

In our initial analysis we observe that, the patent dataset has a field for number of times that a particular patent cited by other patents however, further analysis showed that this field based only on US patents. More clearly, the description of this field is as follows: "Number of times the patent was cited by other US patents". Consequently, we don't have information about citations from other countries and decided to restrict the scope of this question into citation made only by US patents.

Note that actual patents are not only from US, just the number of citation that a particular patent have is calculated only by citation of other US patents.
