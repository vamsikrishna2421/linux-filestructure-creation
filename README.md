# linux-filestructure-creation
## Create file structure of projects with a text file.

For example , We have a specific file structure for maven projects.

Lets suppose we save the file structure in a text file "file.txt"

    ./project
    ./project/src/main/java
    ./project/src/main/resources
    ./project/src/main/filters
    ./project/src/main/webapp
    ./project/src/test/java
    ./project/src/test/resources
    ./project/src/test/filters
    ./project/src/it
    ./project/src/assembly
    ./project/src/site
    ./project/LICENSE.txt
    ./project/NOTICE.txt
    ./project/README.txt	
  
  Run the command 
    
    $ xargs -I {} mkdir -p "{}" < file.txt
    
   Check the file structure with 
    
       $ tree project
       
       project/
    ├── LICENSE.txt
    ├── NOTICE.txt
    ├── README.txt
    └── src
        ├── assembly
        ├── it
        ├── main
        │   ├── filters
        │   ├── java
        │   ├── resources
        │   └── webapp
        ├── site
        └── test
            ├── filters
            ├── java
            └── resources

    16 directories, 0 files



refer:
https://youtu.be/zcHGcIu_65k
