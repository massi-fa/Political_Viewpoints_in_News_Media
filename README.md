# README
# Political_Viewpoints_in_News_Media

## Project Overview

This repository provides a dataset for the automated classification of **claims** related to immigration, associating them with specific **viewpoints**. The data consists of claims extracted from articles, each linked to a viewpoint that describes the stance on immigration. The goal is to support the analysis of immigration-related claims and classify them based on different perspectives.


---

## Folder Structure

### 1. **Claims**

This folder contains the dataset of 402 claims extracted from various articles. The dataset includes the following columns:

- `claim_id`: A unique identifier for each claim.
- `utterance`: The text that represents the claim.
- `actors`: The entities or individuals associated with the claim.
- `actors_info`: Information extracted from Wikidata related to the actors who made the utterance. This includes additional metadata such as the actor's role, background, or other relevant data from Wikidata.
- `article`: The article in which the claim was found.
- `article_url`: The URL of the article.
- `article_archive_url`: The archive URL of the article.

### 2. **Immigration-3k**

This folder contains the dataset used for model training, validation, and testing. The dataset is split as follows:

- **Training set**: 2,303 claims
- **Validation set**: 336 claims
- **Test set**: 669 claims

The dataset includes the following columns:

- `claim_id`: A unique identifier for each claim.
- `utterance`: The text representing the claim.
- `actors`: The entities or individuals associated with the claim.
- `actors_info`: Additional information extracted from Wikidata about the actors who made the utterance.
- `viewpoint`: The viewpoint or stance expressed in the claim. Each viewpoint is composed of:
  - **Title**: A concise label or heading summarizing the core idea of the viewpoint.
  - **Description**: A brief description outlining the core ideas of the viewpoint.
- `viewpoint_id`: A numerical identifier for the viewpoint.
- `article`: The article in which the claim was extracted.
- `article_url`: The URL of the article.
- `article_url_wayback`: The Wayback Machine URL of the article.
- `classification`: The classification label for the claim.

### 3. **Prompts**

This folder contains the templates for the prompts used in different stages of the process:

- **Claims&Actors_extraction_prompt_template**: Template used for extracting claims and associated actors from articles.
- **text_prompt_template**: Template used for fine-tuning and inference tasks related to claim classification.
- **KG_prompt_template**: Template used for integrating knowledge graphs into the model's inference process.
- **Text+KG_prompt_template**: Combined template that integrates both text and knowledge graph information for model fine-tuning and inference.

---