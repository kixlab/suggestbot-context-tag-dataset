# Context-related Hashtag Classification Dataset

This dataset contains the classification of hashtags into a predefined set of context categories.

Hashtags of social media posts contain information on the context of the posts. However, hashtags often consist of only a couple of words, and the set of tags could give a new meaning apart from the meaning of each hashtag. Furthermore, some hashtags contain multiple words without proper punctuation. Such problems make it hard to classify hashtags into appropriate context categories. To overcome such issue, we crowdsourced hashtags and their classifications from Amazon Mechanical Turk by either a) asking workers to share hashtags from their own Instagram posts and classify the tags or b) asking workers to share hashtags by making hypothetical Instagram posts and classify the tags.  

## Data structure

The dataset contains two JSON files. Although they are generated from different crowdsourcing interface, the two files have the identical structure.
Each mapping is represented as a JSON object with the following structure:

{
  "1": {             // Unique ID for each tag
    "text": "beach", // Text of each hashtag. Is is possible that the same tag occurs multiple times by different annotators. .
    "post_id": 233,  // Unique ID for each post the tag was attached to. If the post_id is the same, the tags were on the same picture. 
    "contexts": [    // List of contexts that the tag is related to. It could be possible that the annotator associated the same tag into multiple contexts. 
      "Location"     // Total eight context categories exist: "Emotion", "Mood", "Location", "Time", "Object", "Activity", "Event", "Other"
    ]
  },
  ...
}
