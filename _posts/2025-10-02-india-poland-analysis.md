---
layout: post
title: " India and Poland: A Tale of Two Economies Through Data"
subtitle: "Learning Economics the Analyst’s Way "
date: 2025-10-02
author: Archish Srinivasan
background: /img/posts/20251002.jpg
---

## A brief Introduction
In my previous avatar, I was a Business Intelligence Specialist who helped my stakeholders make data based decisions by creating data pipelines, visualise the data and derive insights from it . Most of my work would involve querying the tables which I knew better than the back of my hand and turn them into metrics which I had developed along with the business teams.
Recently, I decided to take a break from my career for a journey of self-exploration and find out what I loved doing most - travel to nearby forests, play the violin, explore the growing rage of LLMs, trade and lost money and learned it’s not for me, read books and watch inspiring movies perhaps? Turns out what I really loved was working with data. In just two weeks of enjoying a break I got bored and I decided to take on a personal project which would involve data, lots of data, python and graphs to make some sense out of it. 

## Why India vs Poland?

In my quest for a personal data project, the most vital ingredient was - data. Thankfully, there are a lot of public repositories of really valuable data available for free which I could put to use. One such treasure trove of data was the [World Bank Data][1] containing all kind of economic, social and vital population information and available for free. All I had to do was to swim around and find what catches my interest. 
I decided to use it to compare Indian economy to the Polish economy. So, why these two countries? 
1. Indian economy is an amazing economy to analyse.  A country which is blessed with a lot of natural resources and human capital and yet it feels like it underperforms. One question which always fascinated me - Why couldn’t India achieve the kind of growth that economies like China, South Korea and even Malaysia did? 
2. Why Poland? What drew my interest to Poland was the simple fact that both India and Poland went through tremendous transformation post 1991. After the dissolution of USSR, these countries found themselves in similar but different economic crisis - India faced the Balance of Payment Crisis and needed to be bailed out by IMF. Meanwhile, Poland started liberalisation a bit earlier moved by hyperinflation, in 1989, post [Solidarity Movement][2]. It led to dismantling of the communist state and a series of moves liberalising their economy. 
3. However, as I studied these two economies - which went through a completely different ways in growing their economies, I learned the important differences and similarities between these two economies.  I gained deeper insights on how these two countries have improved tremendously in couple of decades. It also gave me a framework on how to understand economies. 
		 
As a data analyst, I approached this with an open mind and started with an Exploratory Data Analysis. My knowledge of economics is rudimentary and based on one course I took in my MBA and reading different books. My expertise lies in sifting through the numbers, like an explorer venturing through unknown terrain, and discover any interesting story, and boy, do I have a story to tell you! 

## Tools Used
As mentioned earlier, the data I used for this was from the [World Bank Data][3]. It’s publicly accessible data with more than 1000 metrics related to development of almost every country in the world. Mouth watering as it was to use such a big treasure trove of free data, I also had to focus on metrics which were relevant for me. To make it simpler, I chose to focus on two countries alone - India and Poland. I also chose to work only with Economic metrics, however, I may use other metrics if it adds important nuance to the analysis. 

Another free resource which I used for doing the actual analysis was [Google Colab][4] . It provides free Python Notebook environment with a lot of analytics libraries pre-installed. I have shared the link to my notebook in the footnotes.

Google Colab comes with built-in AI assistance by Gemini which was quite useful to code the charts as it’s cumbersome to write the entire code for plotting simple graphs. I also used ChatGPT and Gemini extensively to brainstorm my analysis and to help me out in refining my ideas and thoughts. However, I did not use them to write the code for me, it definitely would have written better code than me but coding is a muscle I want to keep building. I also wrote this article to develop a writing muscle. AI is amazing as a supporting tool but I do not think using them to automate everything is a good idea. 

_ Sidenote : I also tried to use it once to act as a manager to make sure I complete this article on time, it didn’t go as I planned and resulted in hilarious scenario, story for another time._

## India vs Poland - Part 1 : Economic Performance

To compare any two countries, the most commonly used metric is GDP. This is the aggregate of everything that an economy produces. However, there are more than one metric for measuring GDP in World Bank Data. GDP could be measured in US $ term, in local currency, in PPP and even there we can choose whether the currency value to be used varies year by year or is constant. 

Apart from GDP, I also checked GDP per capita and Gross National income per capita. Gross National Income includes all the income generated by residents outside of the country. So I plotted the year over year graph for both countries over these metrics. When I plotted the data measured in constant US dollar i.e. values are measured in US dollar and adjusted for time by locking the value of dollar in 2015. 
![][image-1]

The data for Poland is only available from 1991. This is not a problem for my analysis as I am interested to compare their performance post liberalisation anyways. We see that when it comes to overall GDP growth, India has a much steeper curve but when it comes to GDP per capita growth, it’s the other way around. 

I read that it may not be good idea to measure on USD as they may distort the true picture as cost of living may be different in both the countries, so a person in Poland even with higher income could have a lower quality of life than a person in India. So I plotted the same metrics in PPP and I got an almost similar graph. So I decided to use the current USD figures. 
![][image-2]

These graphs can sometimes be misleading because they are on different scales. To have a more clear comparison, I plotted their growth rate year over year.
![][image-3]
This showed something interesting. India’s GDP per capita growth rate relative to Poland was low in the early years but has picked up from 2011 onwards. By breaking the 30 year period into three decades and calculating the CAGR during those 10 years, it became even clearer that India’s GDP per capita has actually improved much better in last 10 years. But Poland’s per capita growth is incredible, remember 3% of a much bigger number is higher than 6% of a smaller number.
![][image-4]

To go a level deeper, I decided to compare the countries across different sectors. The Total GDP is the output of all industries which can broadly be divided into three sectors : Agriculture, Manufacturing and Services. 

## India vs Poland - Part 2: Sectoral Analysis
First let’s do a broad comparison of the Overall Value added by each sector year over year for both the countries and we can see how India’s economy is overall much larger than Poland. 
![][image-5]
Comparing economies of such different scale is not really ideal but we can still make some interesting inferences here. 
1. Poland's farming sector is on a downwards path while India has an upward trend (_Interestingly, the highs and lows in the India graph could be the function of monsoon variability_)
2. Poland’s industry grew particularly since 2000. India seemingly has a steeper upward slope. We can explore this in detail later. 
3. Services is most interesting. India's service sector looks almost hockey stick. Poland also has a moderately good growth here.
Let’s compare how much each sector contributes towards the GDP.
![][image-6]

Some important insights from these graphs when we see the relative percentage of these sectors with GDP:
- Agriculture (Blue) : India was an agrarian economy in the 90s but the share of Agriculture in GDP is coming down rapidly. Meanwhile, Poland's share in Agriculture has been significantly low.
- Manufacturing (green): Both countries had their shares at around 15% in the 90s but while Poland managed to increase its share to near 20s, India's share remained stagnant.
- Industries (Orange) : When construction is added, it shows that India had a lower share of GDP earlier but it saw an increase in 2005 and onwards but dipped again. Poland had a dip earlier but it picked up later.
- Services (Red) : Both countries have a high share of services as a percentage of GDP. While Poland's share is near 60%, India's share has been increasing rapidly. * Poland is a service economy, India is agrarian but turning into a service economy*
Comparing them at per capita level will be more interesting but slightly tricky. We must divide the value added by the population which is employed in the sector. This will give us a comparison of the productivity of an average worker in both economies. 
![][image-7]

This graph  clearly shows that an average worker in India produces less value than a worker in Poland in every sector. What’s interesting is that while the productivity is increasing in both Agriculture and Services in India as compared to Poland, it’s not growing as much in Industries. 

Some key points:
- The difference in productivity could be either due to skill or due to infrastructure. A worker with a PhD  is more likely to produce high value output compared to someone who is less educated but a PhD cannot produce high quality research if they are denied access to computers and libraries. 
- In Sectors like Agriculture, infrastructure plays more role than skill. A more skilled farmer cannot produce 10x the yield from a piece of land unless they have access to fertilisers and equipments like tractors and machines. 
- In Services it could be the other way around. A college graduate can write a piece of code and all they need is a laptop. 
- Manufacturing is somewhere between the two. It requires capital in the form of machinery and assembly lines but it also requires some level of skills. A technologically advanced machine can produce more valuable output but it also requires somebody more skilled to handle it. 
- Comparing India and Poland on agriculture, it’s clear that India is closing the gap between itself and Poland. India has more land available for agriculture and has natural resources like water. Moreover, there is a lot of low hanging fruits like mechanisation and fertiliser use. 
- In Services, both the countries have seen growth but India seems to produce low value per worker in comparison to Poland. This could be because of low skill levels. We can dig deeper here.
- In manufacturing, India is dismal in relation to Poland. This could be because Poland probably produces more high end good with higher technological input. We will dig deeper here as well.

## India vs Poland - Part 3: Deep dive into Manufacturing and Services
### Manufacturing
Worldbank data provides the following categories of Manufacturing:
- Chemicals
- Food, Beverages and Tobacco
- Machinery and transport equipments
- Textiles and Clothes
- Others ( Other manufacturing, a residual, covers wood and related products, paper and related products , petroleum and related products , basic metals and mineral products , fabricated metal products and professional goods , and other industries)
The value was provided as a percentage of Manufacturing Value added. So we needed to multiply to get the value added in each category. 
Plotting the relative percentage of these categories for the countries:
![][image-8]
We can see that these two countries have hardly any difference in how their manufacturing is distributed. 
Plotting the value instead of percentage :
![][image-9]
This shows something interesting. India’s manufacturing grew mainly on account of “Other Manufacturing”. I am keen to do a deep dive on this but don’t have the data. Since this category includes “Petroleum and related products” and based on what I know of the huge refineries setup in Jamnagar, my hunch is that it contributes the most to this but I can’t make any certain statements until I get better data.
Both countries increased their Machinery manufacturing but India saw more growth in almost all the other categories. 

There is one interesting metric which I discovered : Medium and high-tech manufacturing value added (% manufacturing value added)
![][image-10]

Left graph shows the percentage of medium and high tech manufacturing in total manufacturing and we can see that both countries have similar percentage and India’s percentage is slightly higher. The right side graph shows that India has more value added overall for medium and high tech manufacturing. 
### Services
WorldBank data doesn’t provide any category breakup of the Service industry. I will try to explore the data more and see if I can get any metrics which can be used as a proxy. We will explore the breakup in Service Export in the next section.
## India vs Poland - Part 4: Expenditure Analysis
Whatever an economy produces is either consumed by its people, or results in capital formation (in other words - invested or saved) or exported to other economies. 

Plotting these as percentage of their GDP for India and Poland:
![][image-11]
As we can see:
- India consumes a big share of what it produces. This is expected from such a large country. Poland consumes even larger percentage.
- When it comes to Capital formation, India has also shown an increase in percentage from 2005. 
- Export is most interesting to me : Both countries were net importers and their export was negative. However, Poland has become a net exporter since 2010 onwards while India was still a net importer

This is something we can expect from developing countries - a population which consumes most of what it produces and investing for capital asset formation. They also have to import high value items as they don’t have the infrastructure to produce them. This makes them net importer. 

There is a lot to deep dive and explore here but it goes beyond the scope of what I intended with this article. However, I will do a deep dive on exports cause it shows something interesting.

### Export deep dive
Overall, in the data, I could see that the exports have been categorised into Merchandise export and Service Export. Plotting the exports for these two countries showed that while both countries have been growing manufacturing exports, India has been a huge commercial service exporter.
![][image-12]
Exports, of course, are only one side of trade. The value which gets added to GDP is Exports net of Imports and plotting this shows how India is a huge importer of merchandise. 
![][image-13]
This shows that India is heavily reliant on other countries for a lot of goods that it consumes and if not for services, would find it tough to sustain. However, breaking down the merchandise net exports (or net imports based on how you want to call it) shows what leads to this heavy distortion.
![][image-14]
As we can see, India has to import a lot of fuel. It also imports Minerals, Ores and Metals and Manufactured goods. Poland has to import a lot of fuel too but it has improved the export of its Manufactured goods.

Manufactured goods can further be broken into High tech and Medium to Heavy tech exports. If we compare the exports like this, we can see that - 

![][image-15]

Poland has a much higher percentage of Medium and High Tech exports in its Manufacturing exports, almost double of India. However, when it comes to High tech exports,  both countries are roughly similar. 

The breakup of Service net exports reveals how dominant India is in Computer related services. 
![][image-16]
This graph possibly illustrates the huge advantage India holds when it comes to Computer related services due to a large English speaking population which is well versed with Computers. This talent, if utilised well, could be the bulwark of India’s growth in upcoming decades.

## Next Steps - AI model
I am not a career economist and I am not familiar with a lot of the data points which was available in the World Bank data. All I wanted was to approach data with an open mind and discover what I can learn by looking at it. 

To be honest, I started with great enthusiasm thinking that I will discover deep uncovered secrets with the data, I wanted to come up with solutions that India could adopt to emulate high GDP per capita growth like Poland. However, I realise that my lack of expertise in economics cannot be substituted by deeper analysis of data. As was the case when I was at work, I relied on people who had a deeper understanding of their functions to get a framework around my analysis. 

> On his own, without Subject Matter Expertise, an analyst is like a fighter jet pilot without navigation and a destination. 
I plan to overcome my shortcomings by reading more and gaining a deeper perspective of economic principles. 

This doesn’t mean my exercise completely fruitless. This entire exercise was for a novice like me to understand how economies grow by peering through numbers and by sharing it I hope others like me can develop a better understanding. Below is what I have learned of economics from this:
- A large population is more likely to lead to a large GDP
- However, it also could be a curse because the GDP per capita, ie, the productivity of an average worker is often low
- The growth that Poland had in its GDP per capita was phenomenal. While India is growing in recent years but Poland has a higher GDP per capita and it still manages a decent growth
- India is clearly a farming economy transitioning into a service economy while Poland is a Service economy which has a good Industrial base
- If we take GDP as the sum of consumption, Investments and exports - India as a huge population is likely to consume a lot but if it can also produce a lot more and export the surplus then its growth will be tremendous
- Right now, it produces this surplus in Services, particularly Computer related services
- While India is producing more High tech manufacturing but it is not able to export it. Poland is also similar to India when it comes to exporting High tech manufacturing but it exports a higher share of Medium and High tech manufacturing
> India and Poland, though worlds apart, show us two models of transformation. For India, the lesson is clear: services alone won’t suffice — productivity and manufacturing depth must rise. For Poland, the story is one of disciplined integration into global supply chains. For me, this project wasn’t about being ‘right’ but about learning to see economies as living systems through data. And that journey is just beginning.

### Using RAG to learn more
While I used LLMs to help me out but it was primarily to help me with language and coding some graphs. My objective here was to do more on my own so I can develop a habit. As a next step, I would like to make a better AI model which can improve my work. For this, I plan to code what is called an RAG - Retrieval-Augmented Generation. The plan is to use the world bank data and collect pdfs of policy documents and create a Vector database from them. Then I can ask an LLM model to answer my queries while confining to the limited data which will improve the quality of its answer. If successful, I can use it to figure out the effects that the policies have on the country’s GDP. 

Once again, I would like to approach it with a complete open mind. I also plan to add more countries to compare and contrast which can improve my learning even more. I am keen on reading more on this. 

[1]:	https://data.worldbank.org "World Bank Data"
[2]:	https://en.wikipedia.org/wiki/Solidarity_(Polish_trade_union) "Solidarity Movement"
[3]:	https://data.worldbank.org "World Bank Data"
[4]:	https://colab.google "Google Colab"

[image-1]:	GDP%20comparisons%20in%20constant%20dollar.png
[image-2]:	GDP%20comparison%20PPP.png
[image-3]:	Growth%20rate%20graphs.png
[image-4]:	GDP%20per%20capita%20growth%20rate%20broken%20down.png
[image-5]:	GDP%20breakdown%20by%20sector.png
[image-6]:	Percentage%20contribution%20to%20GDP%20by%20sector.png
[image-7]:	Productivity%20per%20worker%20by%20sector.png
[image-8]:	Manufacturing%20category%20percentage.png
[image-9]:	Manufacturing%20Value%20added%20by%20category%20year%20over%20uear.png
[image-10]:	High%20tech%20manufacturing%20comparison.png
[image-11]:	Consumption%20side%20breakdown%20of%20GDP.png
[image-12]:	Merchandise%20and%20Services%20Export.png
[image-13]:	Merchandise%20and%20Commercial%20Services%20Net%20Export.png
[image-14]:	Merchandise%20breakup%20net%20exports.png
[image-15]:	High%20tech%20low%20tech%20manufacturing.png
[image-16]:	Service%20Net%20export%20breakup.png