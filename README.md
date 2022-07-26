# FLIPKART-GRID 4.0
EXTRACT TRENDS FROM SOCIAL MEDIA

## INTRODUCTION
This system was developed by Devanshi Bavaria and Dhruv Shah as part of Flipkart Grid 2022. The aim of this system is to help fashion retailers in identifying trend-setting and best selling products on Flipkart webiste.

## DESIGN
This system is broken down into 3 important parts:

### SCRAPERS
<li>Used to scrape data from various social media. Currently sites which are scraped include trending tweets from twitter.</li>
<li>All this raw scraped data is currently stored on Drive, with links to it being stored on an Atlas database.</li>
<li>These scrapers are designed to run automatically after a fixed amount of time, so that fresh trending data is always being scraped.</li>
<li>Implemented using libraries like selenium, tweepy etc in python.</li>

### MODELS

<ul><li>
Our solution consists of 2 Models. The first model is the colour and category detection model which takes an image as input and helps in determining the type of clothing(Tshirt, trousers) and the colour of the clothing.
  
<ul><li>
Knowing the type of clothing helps in classifying the clothes, and since this is based on images, the internal category name given to the object does not hamper         with our classification(E.g. the site may be classifying tshirts as T-shirts, but this does not affect the image detection model, it will classify all tshirt data       into the 'tshirt' category)
</li></ul>
  
<ul><li>
Knowing the colour of the model helps in preprocessing the image before passing it to the trendiness detection model. This is done using OpenCV techniques like           colour detection, image segmentation, face detection. Using these techniques, during preprocessing, the backgrounds are removed and the image is cropped to just the     object of interest.
</li></ul>
  
</li></ul>

<ul><li>
The second model is the one used to find trending products. This is done by assigning a score( Trendiness score) to each product. The products with a high score have a higher chance of being in trend. The model takes these parameters as input to determine the trendiness score:
<ul><li>Preprocessed image</li></ul>
<ul><li>Date when product was released/scraped</li></ul>
<ul><li>No of likes/Ratings/ views</li></ul>
<ul><li>No of sites referring this product</li></ul>
<ul><li>Comments/Reviews</li></ul>
</li></ul>


## DATASETS
Scraped Data(till today):https://drive.google.com/drive/u/1/folders/134GDKE7i0MdBYcIyab3mKH6LdxFl-ci0<br><br>
Processed Scraped Data:https://drive.google.com/drive/u/1/folders/134GDKE7i0MdBYcIyab3mKH6LdxFl-ci0

## MODEL FILES
Model for predicting Trendiness: https://drive.google.com/file/d/1092MDfexBLnap2q9ijxvEG-GmBfw9my2/view?usp=sharing<br>

Model for predicting Color and Type of garment from image : https://drive.google.com/file/d/1092MDfexBLnap2q9ijxvEG-GmBfw9my2/view?usp=sharing<br>

(Supporting Binary File ): https://drive.google.com/file/d/1-6_5lyHXmDrhEvjJpdQh8jjyXoX-Gvv2/view?usp=sharing
