# ConnectivityMaintenanceVT2020

This repository stores specification files for three- and four-agent systems modeled in Keymaera X theorem prover. 
The files specifying the three-agent system are compatible with Keymaera X version 4.7.4, while the files for the four-agent system are compatible with KeYmaera X version 4.8. 

The three-agent system contains is modeled in a single large file. The file is then duplicated for each Lemma or invariant we wish to prove.

The four-agent system is split into many files containing multiple hybrid programs. These files specify the various interactions between pairs of agents (e.g. agent 1 receives 
information from agent 2, agent 3 receives information from agent 1, etc.). The folders are organized first by the Lemma/invariant, and then the pair of agents the lemma/invariant
is verified for. Only the files containing the necessary interaction between the pairs of agents specified by the invariant are used to verify the invariant. For example, if an 
invariant only concerns agents 1 and 2, then only the files detailing interactions with agent 1 or agent 2 will be used.

To see a proof, simply copy the contents of a file into a new model in KeyMaera X and save. If the file contains a tactic, then clicking "Run Stored Tactic" will produce the proof
for that file. If a tactic is not included or if the prover stalls, then the proof can be manually reproduced following the guidance in the comment section at the head of the file. 

