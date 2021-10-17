# UCU-2021-Distributed-Systems-Replicated-Log-team-8
homework project for UCU 2021 Data Engineering program 

in folder /log1/ you will find a demo video showing these steps.

how to run log1:
-clone the project
-go to folder /log1/dmytro-kryvosheyev
-in case if you want to run the project not in dockers, then run it on different ports:

-run master:   node server.js --port 6000
-run 1st secondary:  node server.js --port 6001
-run 2nd secondary:  node server.js --port 6002
(in case you want more secondaries, add URLs into config.js )

to add the message:
-POST http://127.0.0.1:6000/master/add-message
msg:  {  property1: "any-value",
                          arr: []
                    }
to see the added messages:
-GET 127.0.0.1:6001/secondary/get-all-messages
-GET 127.0.0.1:6002/secondary/get-all-messages  

                 


3 labs = 3 folders
For example, log-1 contains code for Replicated-Log-1
inside /log-1  you see the file "replicated-log-specs-log1.drawio.svg"
It shows the flow, and green blocks show the specs.
For example, in log-1 the specs are:
 
S receives an object:
POST  /secondary/add-message
in rLogMsg format
   body= {
          inc_id: 1,
          msg:  {  property1: "any-value",
                          arr: []
                    }
     }
     
it means that regardless in which language you make the code for Secondary Node, 
this node must have POST  /secondary/add-message   
which expects body request = {
          inc_id: 1,
          msg:  {  property1: "any-value",
                          arr: []
                    }
     }
     
================
