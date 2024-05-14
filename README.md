# midjourney-bias-exploration
Our repository hosts our research as well as data for the Decoding Biases in AI class group project. Our research aims to detect biases in Midjourney.

[Different themes for the website](https://pages.github.com/themes/)

<h1 align="center"><FONT size ="20pt">Decoding Biases in Midjourney</FONT></h1>

 
## Introduction 
### How does Midjourney work?
### Sous-titre 2

## Lit review

A. __Previous researches__

<div 
style="text-align: 
justify">
 
“A prompt is a short text phrase that the Midjourney Bot interprets to produce an image. The Midjourney Bot breaks down the words and phrases in a prompt into smaller pieces, called tokens, that are compared to its training data and then used to generate an image. A well-crafted prompt can help make unique and exciting images.”
Midjourney operates as an image generation platform, relying on proprietary algorithms for its functioning. Users initiate the process by providing prompts, which the system dissects into tokens for analysis. These tokens are then compared against a vast training dataset comprising billions of images. The precise details of the datasets used to train Midjourney are not openly available to the public, but it is likely that a combination of several datasets was used. During extensive research, we identified potential sources such as the Microsoft Common Objects in Context (COCO) dataset, renowned for its 330,000+ images and 2.5 million captions covering around 80 categories of objects, concepts and scenes. Other popular datasets include Visual Genome, with over 108,000 images and 4 million object samples, and Flickr30k, with over 31,000 images and 158,000 text descriptions. It's also conceivable that Midjourney drew on the LAION-400M and LAION-5B datasets, respectively collecting 400 million and 5.85 billion English and multilingual image-text pairs, from web retrievals carried out by a German non-profit organization. In addition, it is alleged that Midjourney may have relied on a potentially illegal database compiling the styles of 16,000 artists, for which they have been sued.
The system leverages two advanced machine learning technologies: large language models and diffusion models. Large language models, akin to those utilized in generative AI chatbots, aid in semantic comprehension of the prompts. This comprehension is translated into numerical vectors, providing a foundation for the subsequent image generation process. Diffusion models play a crucial role in crafting images based on the prompt's essence. Guided by the numerical vectors derived from the language model, diffusion mechanisms navigate the creative landscape, generating images tailored to the prompt.
However, Midjourney's effectiveness may be hindered by linguistic diversity. Primarily trained on English-language data, prompts in other languages, particularly those with grammatical complexity, may yield suboptimal results. To mitigate this, users may craft prompts in their native language and utilize translation tools to enhance performance. Overall, Midjourney stands as a testament to the integration of language processing and image synthesis, offering a glimpse into the potential of AI-driven creativity.

</div>

B. __Representation of the Environment and the Population__

<br>


 

<br>


## Méthodologie

  - constitution des catégories
  - grille d'analyse
  - analyse quanti: justification des 20 images par prompt. 60 images par target d'analyse. compter cmb de target par catégories pour total prompt chaque categorie
  - tableau excel avec criteres de la grille d'analyse: analyse a la main de chaque image
  - collab python pour creer des regression lineaires/etablir des correlations
     
## Results of the Quantitative Analysis


## Bibliography

add sources here
