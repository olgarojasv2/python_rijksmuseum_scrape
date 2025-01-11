# Rijksmuseum's Collection of Portraits Dataset

## Overview

This project showcases the process of scraping data from the Rijksmuseum's online collection using Python. It specifically focuses on extracting information about four paintings from the museum's portrait collection, underscoring the potential of web scraping in art historical research. The resulting dataset is tailored for researchers and is also suitable for training large language models in face image recognition.

## Project Structure

1. Data Collection
2. Corpus Description
3. Tools and Libraries
4. Scraping Process
5. Data Structure
6. Ethical Considerations

## Data Collection

In the Jupyter Notebook titled Rijksmuseum_Portraits_Metadata.ipynb, the process for web scraping is outlined. First, Pandas and BeautifulSoup were imported to facilitate data scraping and visualization. A request was then made to access the entirety of the Rijksmuseum's collections using the following link https://www.rijksmuseum.nl/nl/collectie. To narrow the focus, portraits within the collection were examined using the same technique (requests.get()). This link was utilized to determine the specific corpus: https://www.rijksmuseum.nl/nl/collectie/node/Portretten--a7c5ba17a2c44f96a25b7c8e0f6fa33d?collectionSearchContext=Art&page=1&sortingType=Popularity&facets[0].id=a7c5ba17a2c44f96a25b7c8e0f6fa33d&facets[0].nodeRelationType=HasRijksTheme

From that link, four paintings were selected. All these paintings are in the "public domain."
1. Self-portrait as the Apostle Paul
https://www.rijksmuseum.nl/nl/collectie/object/Zelfportret-als-de-apostel-Paulus--4faa97ed774e6e3f81b76cf3aed6226d?collectionSearchContext=Art&page=1&sortingType=Popularity&facets[0].id=a7c5ba17a2c44f96a25b7c8e0f6fa33d&facets[0].nodeRelationType=HasRijksTheme
2. <u> Self-Portrait Vincent van Gogh </u>
https://www.rijksmuseum.nl/nl/collectie/object/Zelfportret--72f97ac66c33f86b161cd51d62f7d365?collectionSearchContext=Art&page=1&sortingType=Popularity&facets[0].id=a7c5ba17a2c44f96a25b7c8e0f6fa33d&facets[0].nodeRelationType=HasRijksTheme
3. Portrait of Marie Jeanette de Lange
https://www.rijksmuseum.nl/nl/collectie/object/Portret-van-mevrouw-Marie-Jeannette-de-Lange--443eae859f95c387ab0ad79562c98340?collectionSearchContext=Art&page=1&sortingType=Popularity&facets[0].id=a7c5ba17a2c44f96a25b7c8e0f6fa33d&facets[0].nodeRelationType=HasRijksTheme
4. <u> Isabella </u>
https://www.rijksmuseum.nl/nl/collectie/object/Isabella--ead5f623d828c7250ce5413e809b3551?collectionSearchContext=Art&page=1&sortingType=Popularity&facets[0].id=a7c5ba17a2c44f96a25b7c8e0f6fa33d&facets[0].nodeRelationType=HasRijksTheme

## Corpus Description

The Rijksmuseum corpus consists of a list of four paintings belonging to the Rijksmuseum portrait collection. Each entry contains both visual and textual data.

All the information is recompiled in an Annotated Corpus File (.csv), with different categories that will be explored in the next section. All the information recollected and portrayed is in English.

## Tools and Libraries

We used the following Python libraries for web scraping and data processing:
- Pandas: For data manipulation and CSV file creation
- BeautifulSoup: For parsing HTML and extracting data

## Scraping Process

1. Initialize the Python project and import necessary libraries
2. Connect to the target URLs using requests
3. Parse the HTML content with BeautifulSoup
4. Extract relevant data (title, date, description, image URL)
5. Store the extracted data in a structured format (CSV)

## Data Structure

The scraped data is stored in a CSV file with the following columns:

| Column Names | Description |
| ----------- | ----------- |
| Title       | The title of the scraped item |
| Technique   | The technique employed to elaborate the work of art |
| Date        | The date associated with the item |
| Description | A brief description of the item |
| Image URL   | The URL of the associated image |


## Ethical Considerations 

### Rijksmuseum Open Data Policy

Our collection is for everyone. That’s why the Rijksmuseum makes its digitised collections and metadata available in the highest quality. And we don’t ask for anything in return.

### Public domain
Many of the objects in the Rijksmuseum are in the public domain. This means that copyright is no longer applicable and that the objects are public property. The public must be able to reap the benefits of that. You can therefore use digital reproductions of public domain objects made available by the Rijksmuseum without permission being required. For commercial purposes too.

All the digital reproductions and data that we currently publish via our data services are made by the Rijksmuseum. To the extent that copyright and database rights apply to these digital sources, the Rijksmuseum waives these rights by using the Creative Commons Zero (CC0) Public Domain Statement.

When collection objects are free of copyright, this is explicitly stated in the corresponding descriptive metadata. In these cases, the copyright notice states “Public domain”, with a reference to the CC0 Public Domain Statement.

Information extracted from https://www.rijksmuseum.nl/en/research/conduct-research/data/policy 

Consequently, all images and pictures extracted are classified as being within the "public domain." This classification indicates that the information is considered "public property" and may be utilized for research purposes.
