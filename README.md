<H3>ENTER YOUR NAME : Srijith R</H3>
<H3>ENTER YOUR REGISTER NO: 212221240054 </H3>
<H3>DATE:12.05.2024</H3>

<H1 Align="center">Project Based Experiment<H1>
  
### Objective:
Perform sentiment analysis using your Facebook data and count the number of Occurrences of given word in the extracted text for the code given in the following link.
  
### Program:
```
import pandas as pd
from textblob import TextBlob

data = pd.read_csv("fb_sentiment.csv")

# Given name to count occurrences

given_word = "kindle"

# Initialize counters for sentiment analysis and name occurrences

sentiment_counts = {'positive': 0, 'negative': 0, 'neutral': 0}
name_occurrences = 0

# Perform sentiment analysis and count occurrences of the given name

for index, row in data.iterrows(): # Perform sentiment analysis
blob = TextBlob(row['FBPost'])
polarity = blob.sentiment.polarity
if polarity > 0:
sentiment_counts['positive'] += 1
elif polarity < 0:
sentiment_counts['negative'] += 1
else:
sentiment_counts['neutral'] += 1

    # Count occurrences of the given name
    name_occurrences += row['FBPost'].lower().count(given_word.lower())

# Print sentiment analysis results

print("Sentiment Analysis Results:")

# Print occurrences of the given name

print(f"Occurrences of '{given_word}': {name_occurrences}")

```

### Output:
![image](https://github.com/srijithmass/Project-Based-Experiment-AAI/assets/86846530/3efa6667-76d3-4d6b-8b45-a136abdda4d6)


### Inference:

Thus the sentiment analysis using your Facebook data  is performed and the number of Occurrences of given word in the extracted text for the code is counted.
```
