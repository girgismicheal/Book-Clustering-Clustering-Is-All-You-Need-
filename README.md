# Book-Clustering-Clustering-Is-All-You-Need


# Gutenberg
**Project Gutenberg is a library of over 60,000 free eBooks**

![Gutenberg](https://drive.google.com/uc?export=view&id=1bOd8Hiv-sU8Skj1gYR-2cxLUEBIretyZ)


**Recommended to use GPU to run much faster.
But it works well with the CPU also.**
- GPU takes around 40 min, while CPU may take hours.



# Project Methodology

![Gutenberg](https://drive.google.com/uc?export=view&id=1wNirZx5kEzvy5tPnS2pCaP2xX0ugpx5N)

# Project Main Steps

- [Data Exploration](#1)
- [Data Preprocessing](#2)
- [Word Embedding](#3)
  - [BOW](#4)
  - [TF-IDF](#5)
  - [Doc2Vec](#6)
  - [Bert Embedding](#7)
  - [Glove](#8)
  - [Fast text](#9)
  - [Word2Vec](#10)
  - [LDA (Latent Dirichlet Allocation)](#11)
- [Word embedding dictionary](#12)
- [Clustering](#13)
  - [K-Means](#14)
  - [Expectation Maximization (EM)](#15)
  - [Hierarchical](#16)
- [Choosing Champion Model](#17)
- [Error Analysis](#18)
  - [Cosine Similarity](#19)
  - [Word Count](#20)
- [Conclusion](#21)





# <a name="1">Data Exploration</a>
**By discovering the books’ content as shown below:**

> Sense and Sensibility by Jane Austen 1811]\n\nCHAPTER 1\n\n\nThe family of Dashwood had long been settled in Sussex.\nTheir estate was large, and their residence was at Norland Park,\nin the centre of their property, where, for many generations,\nthey had lived in so respectable a manner as to engage\nthe general good opinion of their surrounding acquaintance.\nThe late owner of this estate was a single man, who lived\nto a very advanced age, and who for many years of his life,\nhad a constant companion.

- Many problems have been found in books' content, so we should deal with them.



# <a name="2">Data Preprocessing</a>

**Clean the content of the books by:**
- Removing the word capitalization, unwanted characters, white spaces, and stop words.
- Replacing some patterns.
- Applying lemmatization and tokenization.

**The data after cleaning process**
> delight steelkilt strain oar stiff pull harpooneer get fast spear hand radney sprang bow always furious man seem boat bandage cry beach whale topmost back nothing loath bowsman haul blinding foam blent two whiteness together till sudden boat struck sunken ledge keel spill stand mate instant fell whale slippery back boat right dash aside swell radney toss sea flank whale struck spray instant dimly see veil wildly seek remove eye moby dick whale rush round sudden maelstrom seize swimmer jaw rear high plunge headlong go meantime first tap boat bottom lakeman slacken line drop astern whirlpool calmly look thought thought

**Dataset Building**

![image](/Image/Screenshot_1.png)

- Create a data frame containing 2 columns and 1000 rows representing the books' samples (Sample) and the book name (Label)

**Note:** Before starting to transform words. We split the data into training and testing, to prevent data leakage.



