# Individual Project

This is a project to create a functional chatbot for COSC 310. The user should be able to hold basic conversation with the bot about sports. The role the agent will take is that of a friend, and the user can ask the agent questions about sports. This program uses modified code from https://github.com/nltk/nltk/blob/develop/nltk/chat/util.py which is open source.

## New Features
New features have been implemented in this bot, including a Wikipedia API and a Twitter API

# Wikipeadia API

In order to run the wikipedia API, you will need first run "pip install wikipedia". The wikipedia API adds to the bots intelligence and is activated by the user asking in the format 'what is __', where the blank is the topic the bot searches wikipedia for. The definition of the topic is returned only if the bot finds it on wikipedia, and if that topic is not on wikipedia, the bot throws an exception and replies with a defualt response. The API is very finicky because if the topic is not spelled correctly then it will give a default response.

Example convo:

Tell me about basketball

                                                      Basketball is a team sport in which two teams, most commonly of five players each, opposing one another on a rectangular court, compete with the primary objective of shooting a basketball (approximately 9.4 inches (24 cm) in diameter) through the defender's hoop (a basket 18 inches (46 cm) in diameter mounted 10 feet (3.048 m) high to a backboard at each end of the court) while preventing the opposing team from shooting through their own hoop.
                                                      
Tell me about hockey

                                                      Hockey is a sport in which two teams play against each other by trying to manoeuvre a ball or a puck into the opponent's goal using a hockey stick.
                                                      
Tell me about lebron

                                                      Lebanon ( (listen)), officially known as the Lebanese Republic, is a country in Western Asia.
                

# Twitter API

In order to the twitter API, you will need to run "pip install Tweepy". The twitter API was implemented 
Example convo:

what is the premier league?

                                                       The Premier League is the top division of soccer in England.
                                                       
do you think i could go to a premier league game for $100?

                                                       Sorry. I don't understand currency well. Can you try again?
                                             
i was born in 1999, who won the premier league that year?

                                                       Sorry, I am unfamiliar with that year. Can you try again?

Named Entity Recognition(NER) was implemented into the chatbot using NLTK's tagging and word tokenizer features along with the averaged perception tagger library in NLTK. The bot seeks and extracts each word the user types and breaks it apart with the word tokenizer. It then prints to console each individual words and it's association with the english language.  Associations such as pronouns, verbs, and adjectives are printed along with its tokened key as part of an array that includes all words of the user's input.  This feature helps programmers recognize the sentence structure the user inputs and can articulate additional conversation pair according to the logged inputs.

Example:

my name is James

                                                       [('my', 'PRP$'), ('name', 'NN'), ('is', 'VBZ'), ('james', 'NNS')]
                                                       
I play soccer

                                                       [('I', 'PRP'), ('play', 'VBP'), ('soccer', 'NN')]
                                                       
                                                       
Synonym Recognition was implemented into the chatbot in two different versions, one using the PyDictionary library, the other using NLTK's WordNet. They both function the same, passing words to the libraries which return synonyms for the words. To reduce memory usage only verbs and adjectives are passed to the libraries and then the sentence the user inputed is mutated to see if changing a synonym in will make the chatbot recognize the statement as a pair. We are somewhat restricted by libraries, as some words aren't properly recognized as synonyms, such as 'Best' being a synonym of 'greatest' but 'greatest' not being a synonym of 'best' according to the library. As you can see by the example below, the chatbot will reply with the same response to both statements.

Example:

I witness hockey

                                                          Who is your favourite hockey player?
                                            
I watch hockey                            

                                                          Who is your favourite hockey player?

