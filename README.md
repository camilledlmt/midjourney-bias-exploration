# midjourney-bias-exploration
Our repository hosts our research as well as data for the Decoding Biases in AI class group project. Our research aims to detect biases in Midjourney.

[Different themes for the website](https://pages.github.com/themes/)

<h1 align="center"><FONT size ="20pt">Decoding Biases in Midjourney</FONT></h1>

<br>

## Introduction 

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

B. __Representation of the Environment and the Population__

<br>


  

<br>


## Méthodologie

<br>

  - constitution des catégories
  - grille d'analyse
  - analyse quanti: justification des 20 images par prompt. 60 images par target d'analyse. compter cmb de target par catégories pour total prompt chaque categorie
  - tableau excel avec criteres de la grille d'analyse: analyse a la main de chaque image
  - collab python pour creer des regression lineaires/etablir des correlations

<br>

## Qualitative and Quantitative Analysis

<br>

A. __Representation of the Environment__

<br>

B. __Representation of the Population__

<br>
<br>

  - __Literature__

<br>

<p align="justify">
The literature on biases concerning the population and poverty in the French banlieues reveals a complex interplay of socio-economic factors, historical legacies, and policy shortcomings. 
</p>
<p align="justify">
Statistical analyses highlight disparities in the income distribution and the access to resources between suburbs and urban centers. Even if they are home to a high portion of the population, banlieues receive less state funding compared to other regions, which perpetuates socio-economic inequalities. For instance, the poverty rate inside the Quartiers Prioritaires de la Ville (QPVs) was around 42% in 2016, which is significantly higher than the 12% poverty rate in other areas surrounding the QPVs, underscoring the concentration of poverty in these neighborhoods. (Lefebvre, 2022)
</p>
<p align="justify">
Then, the concept of path dependency, (Harding, 2023), explains how historical and policy factors contributed to constant biases in urban policies. Successive governments have relied on past practices, by primarily focusing on urban renewal rather than addressing the systemic issues underlying social integration and resource distribution. This has resulted in a cycle of ineffective policies in France that are failing to improve the living conditions of banlieue residents, reinforcing negative stereotypes and perceptions.
</p>
<p align="justify">
Lastly, we observe spatial dimensions of poverty in France which reveals that while banlieues show higher median incomes compared to isolated rural regions, they also harbor certain groups of extreme poverty. (Observatoire des Inégalités, 2022). There is a need to move beyond simplistic narratives that categorize banlieues as either affluent or deprived, emphasizing the heterogeneity within these neighborhoods and the diverse experiences of their residents.
</p>
<p align="justify">
Media coverage of suburbs is often negative and stereotypical, focusing primarily on social issues such as poverty, violence, and crime (Donars & Touaf, 2020). This media representation contributes to creating and perpetuating harmful stereotypes, influencing public perception and policy-making. 
</p>
<p align="justify">
Overall, the literature collectively highlights the multifaceted nature of biases towards the population and poverty in French banlieues. From unequal resource allocation to historical legacies of urban planning, these biases are shaping different aspects of the public discourse, policy decisions, and finally, the lived experiences of residents of the banlieues. This section aims to evaluate the degree at which Midjourney also reflects those kinds of biases in regards to the representation of the population of the Banlieues. 
</p>
<br>
<br>

C. __Representation of the Religion__

<br> 
<br>

## Bibliography
<br>

AIExplorer. (2023, January 13). Comment marche MIDJOURNEY? https://aiexplorer.io/actualites-ia/comment-marche-midjourney/ <br>
Ho, K. K. (2024, January 2). Database of 16,000 Artists Used to Train Midjourney AI, Including 6-Year-Old Child, Garners Criticism. https://www.artnews.com/art-news/news/midjourney-ai-artists-database-1234691955/<br>
Hu, J. (2023, April 6). Bias in Midjourney — It’s not just the Representation, it’s the Art Direction. Medium. https://medium.com/@hujason/race-and-gender-bias-in-midjourney-c43e92f515f<br>
King, M. (2022). Harmful biases in artificial intelligence. The Lancet Psychiatry, 9(11). https://www.thelancet.com/journals/lanpsy/article/PIIS2215-0366(22)00312-1/fulltext<br>
Kobie, N. (2023, December 21). Bias in AI: what 200 images of people at work reveal. TechFinitive. https://www.techfinitive.com/features/what-200-job-images-reveal-about-bias-in-ai/<br>
Laion. (n.d.). https://laion.ai/<br>
Lair, N. (2023, November 8). Tags, déchets, bâtiments délabrés : quand l’IA reproduit les stéréotypes sur les banlieues. France Inter. https://www.radiofrance.fr/franceinter/tags-dechets-batiments-delabres-quand-l-ia-reproduit-les-stereotypes-sur-les-banlieues-3334839<br>
Lin, Maire, Belongie, & Bourdev. (2014, May 1). Microsoft COCO: Common Objects in Context. https://paperswithcode.com/paper/microsoft-coco-common-objects-in-context<br>
Maker, A. (n.d.). How Midjourney Was Trained. https://imaigic.com/blog/how-mj-was-trained#:~:text=One%20of%20the%20most%20popular<br>
Midjourney. (n.d.). Midjourney Prompts. Docs.midjourney.com. https://docs.midjourney.com/docs/prompts-2<br>
Rivai, Z. (2023, June 6). When AI Mirrors Our Flaws: Unveiling Bias in MidJourney. Medium. https://medium.com/@zaida.rivai/when-ai-mirrors-our-flaws-unveiling-bias-in-midjourney-1d5ef73b8e99<br>
Stelzel, P. (2023, May 9). Midjourney: Midjourney Tested In Foreign Languages. https://philipp-stelzel.com/midjourney-foreign-languages/<br>
Wankhede, C. (2023, May 15). What is Midjourney AI and how does it work? Android Authority. https://www.androidauthority.com/what-is-midjourney-3324590/<br>
Zhou, M., Abhishek, V., Derdenger, T., Kim, J., & Srinivasan, K. (2024). Bias in Generative AI. Cornell University. https://arxiv.org/pdf/2403.02726<br>

