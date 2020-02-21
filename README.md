As it stands, only the fetching of the raw data and the initial setup of the tables in postgresql is completed.

config.py needs to be ran first to setup the parser for the config options
create_database.py creates the database
create_tables creates the tables including setting up the values for the enum variables
request_api_data.py takes all the data from the api and stores it in a local file so that it can be read later when loading the data into the tables.

-It is confirmed that all the data needed to be entered into the tables can be obtained from the api requests (as in the readtest.py file) but it would still need to be processed before it can be entered into the tables.
    -Data with multiple references needs to be checked for consistency. Some pieces of data, such as the deposit, need to be parsed before it can be entered in its intended file type.
    -The uuid4 would need to be generated.

Various 'if' checks should be replaced by more proper exception handling.

After that, everything that pertains to the fact that the process should run daily would need to be done (i.e. set up the workflow).
The data  would need to be stored 'by date' (instead of having each run of the script replace the existing raw_data file
