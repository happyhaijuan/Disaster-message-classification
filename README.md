# Disaster Response Pipeline Project
### Project Movitation:
Implement a web app classify disaster messages from user by building a machine learing model. After disaster messages being classified, these classified messages could be sent to the appropriate disaster relief agency.
The model is trained on a data set provided by Figure Eight containing real messages that were sent during disaster events, and the messages could have 36 pre-defined categories, and examples of these categories include Aid Related, Medical Help, Search And Rescue, etc.
This is a multi-label task, since a message can belong to one or more categories.

### Project Description:
The project contains three parts:
1. An ETL pipeline to load csv files, transform and clean data and load to a sql database.
   
     data  
     
        ` disaster_categories.csv          # Dataset including all the categories  
        ` disaster_messages.csv            # Dataset including all the messages
        ` process_data.py                  # Data cleaning
       
       
2. A Machine learning pipeline to build model, train model, evaluate model   
    
      model
      
       ` train_classifier.py              #  build, trian, evaluate ML model       
   
3. A web app displays some visualisations for the data and predict categories for new messages    
            
      app     
        
        ` run.py                           # Flask file that runs app
        ` templates   
             ` go.html                      # Classification result page of web app
             ` master.html                  # Main page of web app  
            
           
### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
