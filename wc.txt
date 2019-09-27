#first do pip install wordcloud


from wordcloud import WordCloud, STOPWORDS

dataset = open("lyrics.txt", "r").read()
def create_word_cloud(string):
    cloud = WordCloud(background_color = "white",stopwords = set(STOPWORDS))
    cloud.generate(string)
    cloud.to_file("/home/abhi/Documents/rcode/wordCloud.png")

	
dataset = dataset.lower()
create_word_cloud(dataset)
