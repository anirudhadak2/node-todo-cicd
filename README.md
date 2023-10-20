# node-todo-cicd

Run these commands:


`sudo apt install nodejs`


`sudo apt install npm`


`npm install`

`node app.js`

or Run by docker compose

test

--------------------------------------------


on jenkins   create dockerfile image and push  to the dockerhub repository 
manual jenkins freestyle job 


there are few plugins are required 

   Dashboard  > Manage Jenkins >  Plugins 
   
           Available Plugins  :    Docker 1.4
           
                                               Docker Commons 
                                               
                                               Docker API   3.3.1
                                               
                                               docker-build-step 2.9
                                               
                                               CloudBees  Docker Build and Publish 1.4.0 


                                              -----------------------------------------
                                              
here build steps in freestyle project job  -->    Build Steps :   Execute Shell  
                             
                              docker build -t myimag  . 
                              
                              docker  login  -u  anirudhadak2  -p  $MYPASS 
                              
                              docker tag  myimag  anirudhadak2/mydocimg:myimag 
                              
                              docker  push  anirudhadak2/mydocimg:myimag 
                              
                              docker logout 
                              
                                ----------------------------
                                
                                docker build -t test  . 

                                
docker  login  -u  anirudhadak2  -p  $MYPASS

docker tag  test  anirudhadak2/node-todo:test

docker  push  anirudhadak2/node-todo:test

docker logout 

docker-compose down && docker-compose up -d

docker ps

----------------------------------
give the docker login password as parameter to security purpose 
--------------------------------------------------------------------
