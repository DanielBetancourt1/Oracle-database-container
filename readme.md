# DISCLAIMER
The information provided here regarding the use of Oracle products is solely intended for instructional purposes. Any usage or implementation of these products based on the instructions provided here is done at your own risk and responsibility. It is important to note that this usage is not intended to infringe upon any copyright or terms of use established by Oracle Corporation or any other relevant parties. The instructions provided here were obtained by reading official documentation of Oracle, and the author has no affiliation or relationship with Oracle Corporation. Users are encouraged to review and adhere to the official terms of use and licensing agreements associated with Oracle products before utilizing them in any capacity. The author and publisher of this code disclaim any responsibility for the misuse or unauthorized use of Oracle products based on the information provided herein.

# Advantages
You can use this docker-compose file and add other services (in the same container) to get easy replicable container projects. 
At the same time you can take advantage of the capacity of containers to turn on and off easily while you keep the persistent database files on your host.

# First steps
- Clone this repo
- Copy the .env.example into a new .env file and modify their content accordingly. You can do this by running in console:

    ```bash
    cp .env.example .env
    ```
# How to run:
- Start docker Engine
- Open a console in the project directory 
- build and up the container by running:

    ```bash
    docker compose up
    ```
Wait until the build finish.

# Next steps:
- Install or run your preferred Database administrator

- You may be interested in create a new tablespace

    CREATE TABLESPACE tbspc 
    DATAFILE 'tbspc_data.dbf' 
    SIZE 1m;

- You may be interested in create a user / schema on oracle 

    CREATE USER my_user IDENTIFIED BY mypass;

- Check if it was created successfully

    SELECT username, account_status FROM dba_users
    WHERE username = 'my_user';

- Grant permissions to this user -- Proceed carefully

    GRANT CONNECT TO my_user;

    GRANT CREATE TABLE TO my_user;

# Final thoughts:
    Any recommendations in order to improve the quality, performance or best programming practices are welcome!