## Installing mongodb:

1. Download the required package from [MongoDB community edition](https://www.mongodb.com/try/download/community)
2. ```cd ``` into the downloads folder and type: ```sudo dpkg -i <PACKAGE_NAME>```
3. Check if it has been successfully installed using: ```mongod --version```
4. Start MongoDB server using: ```sudo systemctl start mongod```
5. Check the status using: ```sudo systemctl status mongod```
6. Download the MongoDB Shell ([mongosh](https://www.mongodb.com/try/download/shell)) package and install it using step 2.
7. Type ```mongosh``` in the shell to check if it is working properly.
8. Download the MongoDB GUI ([mongodb-compass](https://www.mongodb.com/try/download/compass)) package and install it using step 2.
9. Run the GUI using: ```mongodb-compass ```
