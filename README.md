# UCU-2021-Distributed-Systems-Replicated-Log-team-8
homework project for UCU 2021 Data Engineering program 

3 labs = 3 folders
For example, log-1 contains code for Replicated-Log-1
inside /log-1  you see the file "replicated-log-specs-log1.drawio.svg"
It show the flow, and green blocks show the specs.
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
