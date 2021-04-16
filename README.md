# Individual Project

This is a project where we create a functional chatbot for COSC 310. The user should be able to hold basic conversation with the bot about sports. The role the agent will take is that of a friend, and the user can ask the agent questions about sports. This program uses modified code from https://github.com/nltk/nltk/blob/develop/nltk/chat/util.py which is open source.

This bot was built off the Assignment 3 that was developed by team 3 in the class COSC 310. The previous repository: https://github.com/COSC-310-Team-3/Assignment-3

ChatbotWithPyDictionary.py is the file where the code executed

Video Link:
## New Features
New features have been implemented in this bot, including a Wikipedia API and a Twitter API

# Wikipedia API

In order to run the wikipedia API, you will need first run "pip install wikipedia". The wikipedia API adds to the bots intelligence and is activated by the user asking in the format 'Tell me about __', where the blank is the topic the bot searches wikipedia for. The definition of the topic is returned only if the bot finds it on wikipedia, and if that topic is not on wikipedia, the bot throws an exception and replies with a defualt response. The API is very finicky because if the topic is not spelled correctly then it will give a default response.

Example convo:

Tell me about basketball

                                                      Basketball is a team sport in which two teams, most commonly of five players each, opposing one another on a rectangular court, compete with the primary objective of shooting a basketball (approximately 9.4 inches (24 cm) in diameter) through the defender's hoop (a basket 18 inches (46 cm) in diameter mounted 10 feet (3.048 m) high to a backboard at each end of the court) while preventing the opposing team from shooting through their own hoop.
                                                      
Tell me about hockey

                                                      Hockey is a sport in which two teams play against each other by trying to manoeuvre a ball or a puck into the opponent's goal using a hockey stick.
                                                      
Tell me about lebron

                                                      Lebanon ( (listen)), officially known as the Lebanese Republic, is a country in Western Asia.
                

# Twitter API

In order to the twitter API, you will need to run "pip install Tweepy". The twitter API was implemented for the use of getting a twitter users most recent tweet. The API is invoked by the user tpying 'show me __ tweets', where the blank is the twitter username. It is not casesensitive even though some twitter usernames have capitals in them, the API treats them all as lowercase. The output even prints out emojis and proper text from the requested users timeline.

Example convo:

show me elonmusk tweets

                                                       @sadiaslayy @DogecoinBets 😮@lexfridman One of many reasons that we need to make life multiplanetary!
                                                       
show me kingjames tweets

                                                       @Rhuigi 🩳 &amp; 🧥 is 🔥🔥🔥🔥🔥🔥🔥🔥🤣🤣🤣🤣🤣🤣🤣🤣🤣. Gotta love it! https://t.co/GqpqgAb3sR
                                             
show me uberfacts tweets

                                                       RT @UberFacts: Due to the bond dogs and humans have had over history, dogs have evolved to understand the meaning of human laughter. They k…Unique facts about the greatest Abstract Expressionist painters 👨🏻‍🎨 https://t.co/NVbzHp4HGq

