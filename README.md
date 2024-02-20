# To run this visualization:
- Clone this repository into a folder on your local PC.
- Open the home.html file and navigate through it on your web browser to view the r/AITA visualizations and analysis.
- You may ignore all the other files.

## Some Notes:
### We tried
1. Bigram analysis with NLTK and the phrase we got were this:
```
(('ncbi', 'nlm', 'nih'), 20.741070180898106)
(('nlm', 'nih', 'gov'), 17.571145179455794)
(('sclient', 'img', 'ei'), 17.28163856226081)
(('lnms', 'tbm', 'isch'), 17.12963546881576)
(('bih', 'biw', 'rlz'), 16.544672968094602)
(('biw', 'bih', '#imgrc'), 16.392669874649556)
…
```
2. Trigram analysis with NLTK:
```
[('burkina', 'faso'),
 ('dua', 'lipa'),
 ('feng', 'shui'),
 ('humpty', 'dumpty'),
 ('humtu', 'nunun'),
 ('hunky', 'dory'),
 ('junji', 'ito'),
 ('margot', 'robbie'),
 ('mont', 'blanc'),
 ('ncbi', 'nlm')]
```
Why we didn’t use both:  Although some of the phrase combinations that showed up were pretty interesting, it didn’t really do a good job of outlining the themes that were the most common in each category.

## Stretch Goals
1. Topic Modeling: Topic Modeling provides us with a list of repeating patterns of co-occurring terms in a corpus. This would have been useful to us since our analysis of the data was more on the bag of word order and using some sort of NLP approach would be another way to confirm that our findings were significant. 
2. Interactivity: Our initial prototype included many interactive elements like mousing over and zooming however, the limitations of the python wordcloud library with the web presented challenges making it difficult to make this happen for our MVP. We tried our best to convey the same information through alternative means (like our bar graphs). 
    - We are aware that d3 has a word cloud visualization library and a stretch goal for us would be to dynamically render a word cloud based on user inputted query parameters (like time ranges, verdict, topic etc.) using flask. This would mean writing logic to route user query to python code, generate a custom list of words and then route that to the front-end for d3 to render. We looked into libraries that scaffold this for us using python however they did not work with WordCloud (Quarto, Genesis, Bokeh).

References:
Some of the html, css and js code was inspired by w3schools.com.
Css - https://watercss.kognise.dev/
Image zooming functionality: https://www.w3schools.com/howto/howto_js_image_zoom.asp
