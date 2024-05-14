# midjourney-bias-exploration
Our repository hosts our research as well as data for the Decoding Biases in AI class group project. Our research aims to detect biases in Midjourney.

[Different themes for the website](https://pages.github.com/themes/)

<h1 align="center"><FONT size ="20pt">Decoding Biases in Midjourney</FONT></h1>

<br>

## Introduction 

<br>
<p align="justify">
The Midjourney algorithm might be known best for its impact on the art world. Indeed, it received [global](https://www.nytimes.com/2022/09/02/technology/ai-artificial-intelligence-artists.html) attention when Jason M. Allen won the Colorado State Fair digital artwork competition in 2022 by using Midjourney to generate his entry (NYT, 2022). This competition generated a  discussion about the future of art, fairness in art competitions, and reminded the public of the increasing capabilities of AI systems. Despite Midjourney’s ability to generate hyper-realistic and high quality artwork, the system has generated controversy due to its apparent biases. In 2023, Heetch, a French VTC company, launched a publicity campaign which put Midjourney’s biases at its centre. It denounced the stereotypes that the algorithm displayed when the word “banlieue” was inserted in a prompt, notably that the environment was often degraded, and people were displayed as sad and poor. 
</p>p
<br>
<p align="justify">
This research builds on Heetch’s publicity campaign by studying the systematic biases displayed by Midjourney against the banlieue. For this purpose, our study aims to analyse environmental biases, poverty biases, and religious biases both qualitatively and quantitatively.
</p>
<br>



### How does Midjourney work?

<br>
<p align="center">
<i> 
“A prompt is a short text phrase that the Midjourney Bot interprets to produce an image. The Midjourney Bot breaks down the words and phrases in a prompt into smaller pieces, called tokens, that are compared to its training data and then used to generate an image. A well-crafted prompt can help make unique and exciting images.” (Midjourney)
</i> </p> <br>
<p align="center">
<img src="https://seeklogo.com/images/M/midjourney-logo-75A1FC1847-seeklogo.com.png" 
width="200"
height="170"/> </p>
<p align="justify">
Midjourney operates as an image generation platform, relying on proprietary algorithms for its functioning. Users initiate the process by providing prompts, which the system dissects into tokens for analysis. These tokens are then compared against a vast training dataset comprising billions of images. The precise details of the datasets used to train Midjourney are not openly available to the public, but it is likely that a combination of several datasets was used. During extensive research, we identified potential sources such as the Microsoft Common Objects in Context (COCO) dataset, renowned for its 330,000+ images and 2.5 million captions covering around 80 categories of objects, concepts and scenes. Other popular datasets include Visual Genome, with over 108,000 images and 4 million object samples, and Flickr30k, with over 31,000 images and 158,000 text descriptions. It's also conceivable that Midjourney drew on the LAION-400M and LAION-5B datasets, respectively collecting 400 million and 5.85 billion English and multilingual image-text pairs, from web retrievals carried out by a German non-profit organization. In addition, it is alleged that Midjourney may have relied on a potentially illegal database compiling the styles of 16,000 artists, for which they have been sued. <br>
The system leverages two advanced machine learning technologies: large language models and diffusion models. Large language models, akin to those utilized in generative AI chatbots, aid in semantic comprehension of the prompts. This comprehension is translated into numerical vectors, providing a foundation for the subsequent image generation process. Diffusion models play a crucial role in crafting images based on the prompt's essence. Guided by the numerical vectors derived from the language model, diffusion mechanisms navigate the creative landscape, generating images tailored to the prompt. <br>
However, Midjourney's effectiveness may be hindered by linguistic diversity. Primarily trained on English-language data, prompts in other languages, particularly those with grammatical complexity, may yield suboptimal results. To mitigate this, users may craft prompts in their native language and utilize translation tools to enhance performance. Overall, Midjourney stands as a testament to the integration of language processing and image synthesis, offering a glimpse into the potential of AI-driven creativity.
</p>

<br>


## Literature review

<br>

A. __A landscape of previous researches about Midjourney’s biases__

<br>
<p align="center">
<img src="https://permutable.ai/wp-content/uploads/2023/12/bias-word-written-color-paper-cards-bias-text-blue-table-your-desing-concept.jpg" 
width="400"
height="240"/> </p>

<p align="justify">
The research findings shed light on various biases present in AI image generation, particularly in the case of Midjourney. The studies reveal pervasive patterns of racial, gender, and age biases, as well as inaccuracies and stereotypes in the generated images.
In the study by Rivai (2023), it was highlighted that Midjourney consistently fails to accurately represent African-American scientists, reflecting broader systemic biases in the technology and AI industry. Similarly, Hu (2023) observed that white individuals are more frequently depicted in modern environments, while people of color are often confined to natural or studio settings. Furthermore, certain clothing styles were found to be associated with specific genders and races, perpetuating stereotypes.
A comprehensive analysis of 200 job-related images conducted by Kobie (2023) unveiled several biases. Gender stereotypes were evident, with women depicted in traditionally male-dominated professions but often portrayed in a stereotypical and youthful manner. Ethnic stereotypes were also prevalent, with underrepresentation of diverse ethnic backgrounds and reinforcement of reductive stereotypes. Additionally, age biases were noted, as images tended to depict professionals as younger than the demographic reality of their respective professions. <br>
The study published by King (2022) investigated Midjourney's representation of mental illness by entering the term "schizophrenia." The generated images depicted grotesque and unnatural facial features, perpetuating harmful stereotypes associated with mental illness and contributing to stigma. <br>
Further corroborating these findings, the research by Zhou et al. (2024) identified systematic gender and racial prejudices across multiple AI generators, including Midjourney. Subtle biases were observed in facial expressions and appearances, reinforcing stereotypes such as depicting younger, happier women and older, angrier men. vv<br>
What prompted us to work on the subject of the representation of the French suburbs by image-generating AI tools such as Midjourney was an article published on France Inter by Noémie Lair (2023). The research revealed that Midjourney's artificial intelligence generates stereotyped images of the French suburbs, representing them as tagged and dirty places, with sad characters surrounded by garbage and graffiti. This bias has been denounced by the VTC company Heetch, which operates mainly in the suburbs and is seeking to change this negative perception by launching a communication campaign. Tests carried out confirm this bias, attributed to Midjourney's use of stereotyped databases. This situation raises the need for an audit of content generation by generative AIs to ensure greater transparency and correct these biases, according to experts. In the meantime, Heetch is hoping to change this negative representation of the suburbs through its communication campaign. We therefore decided to take a closer look at this subject by borrowing an analysis of the images generated by Midjourney in different categories, comparing images of the suburbs (“banlieues”) with the city (“villes”) and the countryside (“campagnes”). <br>
In summary, all of these studies collectively underscore the urgent need for mitigating biases in AI image generation systems like Midjourney. Addressing these biases is essential not only for promoting diversity and inclusion but also for ensuring that AI technologies accurately reflect and represent the complexity of human experiences without perpetuating harmful stereotypes.

<br> <br>

<br>


## Méthodologie

<br>


  - constitution des catégories
  - grille d'analyse
  - analyse quanti: justification des 20 images par prompt. 60 images par target d'analyse. compter cmb de target par catégories pour total prompt chaque categorie
  - tableau excel avec criteres de la grille d'analyse: analyse a la main de chaque image
  - collab python pour creer des regression lineaires/etablir des correlations

<br>


# Qualitative and Quantitative Analysis


<br>


## Literature Analysis

<br>

A. __Representation of the Environment__

<br>

<p align="justify">
The landscape of the banlieues is deeply intertwined with France's post-war urban design choices. Following World War II, a housing crisis gripped the nation due to a surge in urban migration and wartime destruction. In response, the government launched a large-scale social housing program (HLM) in the 1950s, under the ["Plan Courant"](https://francearchives.gouv.fr/fr/pages_histoire/39082). This ambitious plan resulted in the construction of vast housing estates, known as "grands ensembles," on the outskirts of major cities. These estates were dominated by high-rise apartment buildings ("barres"), built with the aim of providing affordable and modern housing for a rapidly growing population.
</p>

<br>

 __Urban design characteristics__

<br>

<p align="justify">
The banlieues, a term often associated with the suburbs of French cities, have become synonymous with high-density housing. Towering above the urban landscape, these high-rise buildings, frequently surpassing 10 stories, pack a large number of residents into a compact space. The architecture of these structures is regularly critiqued for its monolithic design—uniform and lacking diversity, where the rapidity and efficiency of construction took precedence over aesthetic considerations. This has resulted in a limited amount of green space and public areas, with the original urban planning favoring housing blocks over communal gardens, public squares, or places for community engagement. Furthermore, these neighborhoods are typically segregated from city centers, situated on the outskirts with inadequate public transport links, making access to the city’s heart a challenge. The commercial amenities within the banlieues themselves are often scarce, compounding the sense of isolation from the bustling city life.
</p>

<br>

__Criticisms and Modernization Efforts__ 

<br>

<p align="justify">
The banlieues, often stigmatized for unemployment, crime, and social unrest, have long been the subject of critical discourse. Critics point to the very fabric of urban design as a catalyst for these issues, suggesting that the layout promotes isolation, curtails opportunities, and engenders a pervasive sense of disenfranchisement among residents.
</p>
<br>
<p align="justify">
In response to these challenges, recent decades have witnessed concerted efforts to breathe new life into these suburban areas. Demolition and reconstruction initiatives have seen some of the most dilapidated housing blocks razed to make way for lower-density, mixed-use developments. Urban renewal projects have focused on enhancing public spaces, introducing verdant areas, and fortifying public transportation networks. Alongside these physical transformations, there has been a marked emphasis on social programs aimed at bolstering social services, broadening educational prospects, and fostering community engagement, all in a bid to reinvigorate the banlieues and their inhabitants.
</p>
<br>
<br>

B. __Representation of the Population__

<br>
<br>

  - __Literature__

<br>

<p align="justify">
The literature on biases concerning the population and poverty in the French banlieues reveals a complex interplay of socio-economic factors, historical legacies, and policy shortcomings. 
</p>

<br> <br>

<p align="justify">
Statistical analyses highlight disparities in the income distribution and the access to resources between suburbs and urban centers. Even if they are home to a high portion of the population, banlieues receive less state funding compared to other regions, which perpetuates socio-economic inequalities. For instance, the poverty rate inside the Quartiers Prioritaires de la Ville (QPVs) was around 42% in 2016, which is significantly higher than the 12% poverty rate in other areas surrounding the QPVs, underscoring the concentration of poverty in these neighborhoods. (Lefebvre, 2022)
</p>
<br> <br>
<p align="justify">
Then, the concept of path dependency, (Harding, 2023), explains how historical and policy factors contributed to constant biases in urban policies. Successive governments have relied on past practices, by primarily focusing on urban renewal rather than addressing the systemic issues underlying social integration and resource distribution. This has resulted in a cycle of ineffective policies in France that are failing to improve the living conditions of banlieue residents, reinforcing negative stereotypes and perceptions.
</p>

<br> <br>

<p align="justify">
Lastly, we observe spatial dimensions of poverty in France which reveals that while banlieues show higher median incomes compared to isolated rural regions, they also harbor certain groups of extreme poverty. (Observatoire des Inégalités, 2022). There is a need to move beyond simplistic narratives that categorize banlieues as either affluent or deprived, emphasizing the heterogeneity within these neighborhoods and the diverse experiences of their residents.
</p>

<br> <br>

<p align="justify">
Media coverage of suburbs is often negative and stereotypical, focusing primarily on social issues such as poverty, violence, and crime (Donars & Touaf, 2020). This media representation contributes to creating and perpetuating harmful stereotypes, influencing public perception and policy-making. 
</p>

<br> <br>

<p align="justify">
Overall, the literature collectively highlights the multifaceted nature of biases towards the population and poverty in French banlieues. From unequal resource allocation to historical legacies of urban planning, these biases are shaping different aspects of the public discourse, policy decisions, and finally, the lived experiences of residents of the banlieues. This section aims to evaluate the degree at which Midjourney also reflects those kinds of biases in regards to the representation of the population of the Banlieues. 
</p>

<br>
<br><br>

  - __Analysis__

<br><br>

<p align="justify">
Categories in this section include: persons, men, women, children, families, and young people. 
</p>

<br> <br>

<p align="justify">
Initially, what stood out and allowed us to quickly elaborate a robust analysis grid, were some criteria that were recurring when prompting for the banlieues: cold atmosphere, people living in poor conditions and that do not seem happy overall. 
</p>

<br> <br>

<p align="center">
<img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/correlation%20heatmap.png?raw=true" 
width="800"
height="600"/> </p>

<br> <br>

<p align="justify">
Criteria that show the highest correlations with the banlieue are cool colors (0.68), sad atmosphere (0.68), black skin/people of color (0.72), presence of graffitis (0.88) and degraded environment (0.92). On the contrary, factors like joyful atmosphere, warm colors and good condition environment are highly negatively correlated with the banlieue. For the cities, it is the opposite; we found a high correlation with the good condition environment criteria (0.91) as well as with a joyful atmosphere (0.63). Let’s see how those criteria appear in some bar plots  and linear regressions representations: 
</p>

<br><br>

<div style="text-align: center;">
  <img src="https://raw.githubusercontent.com/camilledlmt/midjourney-bias-exploration/0b9142e8b2f44d3303e11a63696f4e4393a5a2d8/good%20contiion%20environment.png" width="350"/> <img src="https://raw.githubusercontent.com/camilledlmt/midjourney-bias-exploration/0b9142e8b2f44d3303e11a63696f4e4393a5a2d8/degraded.png" width="350"/>
</div>

<br> <br>

<p align="center">
<img src="https://raw.githubusercontent.com/camilledlmt/midjourney-bias-exploration/0b9142e8b2f44d3303e11a63696f4e4393a5a2d8/banlieue%20degraded.png" 
width="750"
height="500"/> </p>

<br> <br>

<p align="justify">
For the criteria regarding the condition of the environment, we chose not to include the location of the campagne, mainly because it mostly only displayed fields or natural elements in the background of the pictures. Therefore, it was impossible to evaluate the living conditions of the people that were depicted in the outputs. Globally, we observe a very clear distinction between the living conditions between the banlieues and the cities. Conditions are depicted in a very deplorable way in the banlieue, where the surroundings represented seem at best only degraded, and in the worst cases even completely abandoned, whereas the cities usually represent typical French streets, similar to those you would see in Paris for example, except for some exceptions. Here are representative outputs of the global environment in both banlieues and cities: 
</p>

<br> <br>

<div style="text-align: center;">
  <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/enfant%201.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/enfant%20ville%202.png?raw=true" width="300"/>
</div>
“Photo réaliste d’un enfant en France dans une banlieue” vs “Photo réaliste d’un enfant en France dans une ville”

<br> <br>

<div style="text-align: center;">
  <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/cool%20colorss.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/warm%20colorss.png?raw=true" width="300"/>
</div>

<br> <br>

<div style="text-align: center;">
  <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/sad%20atm.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/joyful.png?raw=true" width="300"/>
</div>

<br> <br>

<p align="justify">
Our first assumption before prompting and at the very beginning was that the pictures that would be generated relating to the banlieues were going to be mostly depicting a gloomy and cold atmosphere, with pictures mainly composed of cool and cold colors. Turns out that given our quantitative analysis, we were right. As shown by Figures XXX and XXX, the majority of the outputs showing a sad atmosphere and cool colors are located in the banlieues. However, we did not anticipate the pictures for the cities to have that much cool colors in them and we rather thought that they would have less been correlated with this criteria. Moreover, if you generally won’t find a very joyful atmosphere in the banlieues, it is not absolutely rare to encounter a sad atmosphere in the cities or in the countryside, as shown by Figures XXX and XXX. Here is a sample of our outputs concerning families : 
</p>

<br> <br>

<div style="text-align: center;">
  <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/famille%202.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/famille%20campagne%202.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/famille%20ville%203.png?raw=true" width="300"/>
</div>

<br> <br>

banlieue campagne ville

<br> <br>

<div style="text-align: center;">
  <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/grafitis.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/black%20skin%20ppl%20color.png?raw=true" width="300"/>
</div>

<br> <br>

<p align="justify">
One of the very first criteria that we wanted to include onto our analysis grid was the “presence of graffitis”, seeing how recurrent they were for the banlieues, in practically every generated picture for this location, as shown by Figure XXX. A surprise for us in this category was the underrepresentation, globally, of black people/people of colour. Even if they are most represented in the banlieues, that number is not very high compared to the total number of outputs, and additionally, they are not represented in the countryside at all, and only by a very small number in the cities. 
</p>

<br> <br>

<p align="center">
<img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/banlieue%20graffitis.png?raw=true" 
width="750"
height="500"/> 
</p>

<br> <br>

<div style="text-align: center;">
  <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/homme%202.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/femme%203.png?raw=true" width="300"/>
</div>

<br> <br>

<p align="justify">
You can observe the presence of graffitis in Pictures XXX and XXX. Another comparison observable on those two pictures is the general presentation of the people depicted: whereas the men on Picture XXX seem to be “dirtier”, with clothes of less quality, and have faces that show more wrinkles and marks from their way of life, the women on Picture XXX are displayed wearing clothes that seem more casual than used, and they seem to show quite acceptable hygiene. That disparity is observable if you compare pictures of women or men in the banlieues, for some reason.
</p>

<br> <br>

C. __Representation of the Religion__

<br> 
<br><br>

__Religion in France__
<br>
<p align="justify">
Midjourney appears to replicate existing religious biases prevalent in France. Amongst prompts demanding religious or believing people, the generated imagery predominantly featured Christians and Muslims, with no representation of other faiths. This observation may partly be attributed to the dominance of Christianity and Islam within the French demographic landscape, comprising 29% and 9% of the population, respectively (Gautier, 2023; Dille, 2023). Nonetheless, religious diversity in France extends beyond these two major religions. Notably, the nation accommodates one of the largest Jewish communities in Europe, constituting 1% of the population, alongside adherents of Buddhism, Sikhism, Shintoism, among others (Gautier, 2023). This disparity in representation was substantiated through both qualitative and quantitative analyses. As illustrated in Figure X, Muslims are predominantly depicted in banlieues, while Christians are portrayed in rural areas (campagnes). However, these correlations lack statistical significance.
</p>
<p align="center">
<img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/heatmap%20religion%20new.png?raw=true" 
width="800"
height="600"/> </p>
<br>
<div style="text-align: center;">
  <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/religion%201.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/religion%202.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/religion%203.png?raw=true" width="300"/>
</div>
<p align="justify">
Lack of religious diversity was particularly evident in villages, where depictions overwhelmingly portrayed Christianity as the sole religious affiliation. It is a straight contrast with suburbs where the majority of individuals there were Muslims. Moreover, individuals identified as Buddhists were predominantly depicted as people of colour, a correlation supported by quantitative analysis, revealing a statistically significant positive relationship between these variables (0.75). Additionally, a notable demographic trend emerged, with a majority of individuals depicted as elderly, a finding supported by the data presented in Figure X (0.46). The portrayal of Jews by Midjourney was characterised by a sad atmosphere and historical photographs in black and white colours. Christians were predominantly of white skin colour - highlighted by the significant positive correlation in Figure X (0,63). 
</p>
<br>

__Religious prejudice against Muslims__
<br>

<p align="justify">
France has one of the largest Muslim communities in Europe, comprising nearly 9 % of its total population (Dille, 2023). However, their situation is not favourable as they face various forms of discrimination. Particularly striking is the overrepresentation of Muslims in the prison population, constituting between 40% and 50%. In 2019, the study found that 42 % of Muslims living in France feel discriminated against, while the number reaches 60 % for women who wear veils (Dille, 2023). Among other factors, these sentiments stem from state policies aimed at upholding "laïcité" (secularism) and general societal stereotypes. A study conducted in 2012 concluded that 80 % of French society is of the opinion that Islam is incompatible with the principle of laïcité. Prejudices held by the society against Muslims are fuelled by media coverage and political statements that tend to associate Islam with terrorism and radical worldviews (Abdeslam, 2019). In response to a series of terrorist attacks occurring in France, president Macron went as far as to state that “Islam is a religion that is in crisis all over the world today” (Al Jazeera, 2020). Marine Le Pen, leader of opposition party Rassemblement National,  compared Muslims to Nazis during WW2 (Maksic & Ahmic, 2020). Media often report on Islam in a stereotypical and fear-mongering manner, tying the religion with extremism and incompatibility with French values (Abdeslam, 2019). This is translated into the views held by the public as 72 % of the French population is concerned about the possibility of extremism in Islam (Dille, 2023). All of these discriminatory practices and perspectives are replicated and even exaggerated by the AI.//
</p>
<br>
<p align="justify">
When generating images based on prompts for "personnes musulmanes" (Muslim individuals), a consistent pattern emerged in their characteristics. Faces of people were predominantly covered, women were wearing burqas or niqabs, and there were no people of colour in the pictures. In addition, all photos generated of Muslims were displaying creepy, scary, and slightly angry people situated in the darker background indicating violent associations that AI has with this religious minority. It might partially reflect the bias present in French society as Islam is often associated with extremism. In one instance, Midjourney provided us with a photo depicting women with dark circles around her eyes that might either reflect her tiredness or result from a violent action. Such a phenomenon was not observed in any other case. The most notable examples are photos of Muslims man holding guns that were produced for the prompts “photo réaliste de des musulmans en France dans une banlieue” and “photo réaliste de personnes croyantes en France dans une banlieue.” Presence of a gun or any other indication of violence was not displayed for any other religion. 
</p>
<br>
<div style="text-align: center;">
  <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/gun1.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/gun%202.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/gun%203.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/gun%204.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/gun%205.png?raw=true" width="300"/>
</div>
<br>
<p align="justify">
The findings from the quantitative analysis align with this observation, demonstrating a notable positive correlation coefficient of 0.75 between Muslims and violence. To further elucidate this relationship, we constructed scatter plots with linear regression lines for both Muslims and Christians/no religion. While for Muslims we observed positive relationships with violence, Christians and individuals with no religious affiliation displayed a negative correlation. This accounts for strong anti-muslim bias present within the scrutinized AI model.
</p>
<br>
<div style="text-align: center;">
  <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/muslims%20violence.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/christians%20violence.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/sum%20of%20violence%20new.png?raw=true" width="300"/> 
</div>
<br>
<p align="justify">
We could observe a higher rate of violence in the suburbs compared to villages and cities. This trend is clearly illustrated in Figure X, where a positive correlation coefficient of 0.26 between suburbs and violence contrasts with a negative correlation coefficient of -0.26 between cities and violence.
</p>
<br>
<div style="text-align: center;">
  <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/banlieue%20violence%20corr.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/ville%20violence.png?raw=true" width="300"/> <img src="https://github.com/camilledlmt/midjourney-bias-exploration/blob/main/campagne%20violence.png?raw=true" width="300"/> 
</div>
<br>



## Bibliography
<br><br>
Abdeslam, A. (2019). The Representation of Islam and Muslims in French Print Media Discourse: Le Monde and Le Figaro as Case Studies. Journal of Muslim Minority Affairs 39(4). <br>
<br>
AIExplorer. (2023, January 13). Comment marche MIDJOURNEY? https://aiexplorer.io/actualites-ia/comment-marche-midjourney/ <br>
<br>
Al Jazeera. (2020, October 2). Macron says Islam “in crisis”, prompting backlash from Muslims. https://www.aljazeera.com/news/2020/10/2/macron-announces-new-plan-to-regulate-islam-in-france <br>
<br>
Dille, J. (2023). Religious Discrimination against Muslims in France. Ballard Brief. https://static1.squarespace.com/static/5f088a46ebe405013044f1a4/t/64186e893ea01c1e7843ca07/1679322763802/JacksonPDF.pdf <br>
<br>
Donars, A., & Touaf, N. (2020, February 16). La couverture médiatique des banlieues. La Nouvelle Chronique. https://lanouvellechronique.com/2020/02/16/la-couverture-mediatique-des-banlieues/ <br>
<br>
Gautier, M. (2023). La Religion en France - Faits et chiffres. Statista. https://fr.statista.com/themes/3234/la-religion-en-france/#topicOverview <br>
<br>
Guilbeault, M. (2023, July 13). Les banlieues, sous le radar des médias. La Croix. https://www.la-croix.com/France/banlieues-radar-medias-2023-07-13-1201275251 <br>
<br>
Harding, P. (2023, March). Global Challenges - Urban Morphology & Violence. Global Challenges. https://globalchallenges.ch/issue/special_2/stagnation-in-the-french-banlieues/ <br>
<br>
Ho, K. K. (2024, January 2). Database of 16,000 Artists Used to Train Midjourney AI, Including 6-Year-Old Child, Garners Criticism. https://www.artnews.com/art-news/news/midjourney-ai-artists-database-1234691955/ <br>
<br>
Hu, J. (2023, April 6). Bias in Midjourney — It’s not just the Representation, it’s the Art Direction. Medium. https://medium.com/@hujason/race-and-gender-bias-in-midjourney-c43e92f515f <br>
<br>
King, M. (2022). Harmful biases in artificial intelligence. The Lancet Psychiatry, 9(11). https://www.thelancet.com/journals/lanpsy/article/PIIS2215-0366(22)00312-1/fulltext <br>
<br>
Kobie, N. (2023, December 21). Bias in AI: what 200 images of people at work reveal. TechFinitive. https://www.techfinitive.com/features/what-200-job-images-reveal-about-bias-in-ai/ <br>
<br>
Kokoreff, D. M., & Lapeyronnie, D. (s. d.). The French Banlieue: Renovating the Suburbs. <br>
<br>
Laion. (n.d.). https://laion.ai/ <br>
<br>
Lair, N. (2023, November 8). Tags, déchets, bâtiments délabrés : quand l’IA reproduit les stéréotypes sur les banlieues. France Inter. https://www.radiofrance.fr/franceinter/tags-dechets-batiments-delabres-quand-l-ia-reproduit-les-stereotypes-sur-les-banlieues-3334839 <br>
<br>
Lefebvre, I. (2022, June 28). Life in France’s Banlieues: Overview and Battle Plan. Institut Montaigne. https://www.institutmontaigne.org/en/expressions/life-frances-banlieues-overview-and-battle-plan <br>
<br>
Lin, Maire, Belongie, & Bourdev. (2014, May 1). Microsoft COCO: Common Objects in Context. https://paperswithcode.com/paper/microsoft-coco-common-objects-in-context<br>
Madse, M. C. (s. d.). Banlieues 89: Urban Design and the Urban Question. <br>
<br>
Maker, A. (n.d.). How Midjourney Was Trained. https://imaigic.com/blog/how-mj-was-trained#:~:text=One%20of%20the%20most%20popular <br>
<br>
Maksic, A. & Ahmic, N. (2020). Constructing the Muslim Threat: A Critical Analysis of Marine Le Pen’s Twitter Posts During the 2017 French Election Campaign. Journal of Regional Security 15(1) <br>
<br>
Midjourney. (n.d.). Midjourney Prompts. Docs.midjourney.com. https://docs.midjourney.com/docs/prompts-2 <br>
<br>
Observatoire des Inégalités. (2022, October 12). Ville, périurbain, campagne : qui est riche, qui est pauvre ? Observatoire Des Inégalités. https://inegalites.fr/Ville-periurbain-campagne-qui-est-riche-qui-est-pauvre <br>
<br>
Rivai, Z. (2023, June 6). When AI Mirrors Our Flaws: Unveiling Bias in MidJourney. Medium. https://medium.com/@zaida.rivai/when-ai-mirrors-our-flaws-unveiling-bias-in-midjourney-1d5ef73b8e99 <br>
<br>
Stelzel, P. (2023, May 9). Midjourney: Midjourney Tested In Foreign Languages. https://philipp-stelzel.com/midjourney-foreign-languages/ <br>
<br>
Wankhede, C. (2023, May 15). What is Midjourney AI and how does it work? Android Authority. https://www.androidauthority.com/what-is-midjourney-3324590/ <br>
<br>
Zhou, M., Abhishek, V., Derdenger, T., Kim, J., & Srinivasan, K. (2024). Bias in Generative AI. Cornell University. https://arxiv.org/pdf/2403.02726 <br>
<br>

