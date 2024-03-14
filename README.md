#Goal:
This project aims at implementing a community garden startup toolkit for the community of Los Angeles, specifically those impacted by food deserts..  I ensured to extract various legal information on zoning, planning, and permit issuance through online government resources specific to California and Los Angeles to create visualizations and a legally transparent chatbot for guidance.

#Important Information 
In adherence to OpenAI's API policy, cloning and running of my chatbot can cause termination of my API, as it violates their guidelines. Even with env variables, there is still posibility of leak detecetion.  For your effeciency, I have created a brief walkthrough video where I demo the UI locally

https://vimeo.com/manage/videos/923511824

#Project Steps: 
Data Extraction
This project began with the data extraction step.  I compiled data across government websites on policies regarding zoning, community garden policies, and obtaining a permit in Los Angeles. These raw .pdf, .txt, and .csv files are all included in the repository.  This process used API integration, web scraping, and pdf conversion skills

#NLP
After compiling raw text data, I ensured to preprocess this data using NLP techniques.  I used tools such as tokenization, stopword removal, lemmatization and lowercasing through libraries like NLTK.  I then structured this data into a conversational format in“qanda.csv”. This step was to ensure my chatbot could behave in a normal conversational manner.  

#Chatbot setup (App.py)
My script begins by loading in my csv file, and vectorizing it to build a matrix out of the text.  This then allows me to create embeddings.  I used FAISS and OpenAIEmbeddings in order to run a similarity search. I then defined my large language model, and provided it with a template on how I would like it to behave.  This step required fine tuning along the way.  I then ran basic functions to generate a response based on best practiced methods that were defined in my csv. 

#Visualizations
I created 2 maps that serve as informational purposes.  The first map highlights pre existing community gardens in Los Angeles, the second uses my zillow web scrape information as an input to identify unoccupied land for sale in Los Angeles, showcasing the potential for a future with more possible gardens. 

#App Layout
I used Dash for my app layout, as it seamlessly integrated my chatbot and visualizations.  Once running, I added html code to specify how I wanted the UI to be presented.  My chatbot and visualizations are now running successfully on a private url. (Demonstrated in watch.me.mp4)

#Adjustments and fine tuning (current)
In contact with the previous professor on the best ways to deploy this for the community. I am also always looking for opportunities to strengthen and improve my code, I am open to any criticism or evaluation.  
