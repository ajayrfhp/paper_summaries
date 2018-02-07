* Basic Idea
  * Use emojis in tweets as labels to learn representation for words. Use learned representation to do NLP. 
* Data
  * Use large number of tweets. Any set of tweets should do. 
  * Collect tweets. 
  
     `["@SpaceX launched Falcon Heavyyyyy yesterday at 12 45 😄😆"]`
  * Sentence to word tokenization. 
  
    `[ "@SpaceX", "launched", "Falcon", "Heavyyyyy", "yesterday", "at", "12 45", "😄😆"]`
  * Stemming
  
    `["@SpaceX", "launched", "Falcon", "Heavy", "yesterday", "at", "12 45", "😄😆"]`
  * Special token for URL, numbers and twitter handles. 
  
    `["SPL", "launched", "Falcon", "Heavy", "yesterday", "at", "SPL", "😄😆"]` 
    
  * Split text to X and y. 
  
    `X =  ["SPL", "launched", "Falcon", "Heavy", "yesterday", "at", "SPL"]`
    `y = ["😄😆""]`
  * Expand multiple emojis in one sentence to multiple examples. 
  
    `X =  [ ["SPL", "launched", "Falcon", "Heavy", "yesterday", "at", "SPL"], ["SPL", "launched", "Falcon", "Heavy", "yesterday", "at", "SPL"]]`
    `y = ["😄", "😆"]`
  
  * Emojis are one hot encoded after conversion to an integer. Emoji classification problem. 
  
    `y = [ [0,0,0,0,1...], [0,1,0...] ]`
  
  * Shape of X = `( Number of tweets, max_word_len )`.
  
    Shape of y = `( Number of tweets, number_of_emojis )`
  
* Model architecture
    
   * Data `( Number of batches, max_word_len )`
   * Embedding Layer 
   
    `Embedded output = Data * Embedding matrix `
    
    
    
    
    
* Computational resources
* Results
* What was new
* Comments

