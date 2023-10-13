# Automatic Data Capture for Borehole Data on Depth to Bedrock and Surficial Stratigraphy in Northern Canada

## 1.	Introduction

Portable Document Format, or PDF documents, are one of the most popular and commonly used file formats for knowledge and information transfer. As the world rapidly moves to a digital economy, PDFs have also become an environmentally-friendly alternative to paper, allowing creators to easily share, print and view a file in its intended layout on multiple platforms. They hold a wealth of important information for organizations, businesses and institutions in a format that reflects the paper it replaced.  

Although PDFs are a reliable way to format and store data, attempting to scrape, parse or extract their data can be a challenging task. Many companies are leveraging the power of responsible artificial intelligence (AI) technologies and applying data science solutions to research and build solutions that can mine valuable insights from unstructured sources like PDFs and scanned images. Applying these solutions could saves costs and time providing accurate information to everyone. By obtaining and extracting data from PDF documents, we can devise ways to generate high-quality meaningful statistics in a timely manner. This has the potential to save a significant amount of time in capturing the data and allows researchers to focus their time on more meaningful analysis.  

The Geological Survey of Canada has created a depth to bedrock surface for all of Canada. However, most of Canada lacks subsurface data support for a depth estimation and hence the mapping process relies on proxy data, such as surficial geology mapping. Due to data support issues the reliability of this map for much of the Canadian Shield and orogenic belts of Canada is poor. The problem of borehole data support is particularly acute in northern Canada where existing territorial databases only have metadata (e.g. https://www.miningnorth.com/chamber-news/101612) with no stratigraphic information for either surficial sediment cover or bedrock. Existing published global estimates are similarly constrained by a complete absence of subsurface data. To advance methods development using Machine Learning approaches and to quantify uncertainty ranges subsurface data is an essential component. The need and value of subsurface data integrated by proxy data has been demonstrated through work in northern Saskatchewan. Most of the time, this data is scattered among thousands of reports and borehole logs which requires manual scraping to find relevant data which costs a lot of person-time and the risk of input errors is high. There is therefore a need for a robust automatic data extraction method for information in text, figures and data tables of PDF files. 

## 2. Developed codes:
  - The function (get_pdf_type_summary.py) is developed to get a summary of all pdf files in the dataset.
  - The SCS file includes 3 functions:
    - The first function (separate_pdf_type.py) searches through all files and folders (and subfolders) of an input directory and finds files with the “.pdf” extension, reads the metadata of the pdf files and separates them into pdfs with searchable text and pdfs which are scanned or mixed.  
    - Second function (To_selectable_text_convertor.py) converts the latter category into images and then uses Optical Character Recognition (OCR) to convert images to pdfs with searchable text.  
    - Last function (get_borehole_pdf.py), searches through all pdfs, finds and copies the ones that contain keywords determined by the user into a destination folder.  

## 3.	Summary of Findings
The application of open-source pdf information extraction tools on borehole logs were investigated using data from the Northwest Territories Geological Survey (NTGS) online library. This data was analyzed to check the feasibility of developing an algorithm for automatic extraction of depth to bedrock and borehole metadata from borehole logs in pdf format. To achieve this goal, first a preprocessing pipeline was developed to convert scanned pdfs to searchable pdfs and select relevant pdfs. With this pipeline any user can find the relevant pdf files from thousands of files quickly and accurately. Selection can be refine using specific keywords.  

Next, the performance of five different tools were evaluated in their capability to extract information from pdf borehole logs. It was seen that tools that export information as tables generally perform better than the ones that export information in text format because they can keep the spatial position of relevant texts such as description and depth which are usually situated in front of another.  

Finally, a subset of 50 borehole logs in pdf format were studied in detail. This analysis showed that all pdf borehole logs (and pdf files in general) are unstructured in nature and therefore creating a text-based information extraction algorithm would need to be case specific which is in contradiction with the overall goal of the project. Application of other advanced approaches such as machine learning should be considered. However, the limited time and resources of this study did not allow it since this approach requires an a priori database for learning phase.

## 4. Contact Information
For questions contact: 
Nicolas Benoit (Nicolas.Benoit@NRCan-RNCan.gc.ca)
Afshin Amini (afshin.emd@gmail.com)

### © His Majesty the King in Right of Canada, as represented by the Minister of Natural Resources, 2023
