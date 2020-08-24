# ConnectivityMaintenanceVT2020

This repository stores specification files for three- and four-agent systems modeled in Keymaera X theorem prover. 
The files specifying the three-agent system are compatible with Keymaera X version 4.7.4, while the files for the four-agent system are compatible with KeYmaera X version 4.8. 


# Directory Structure

The three-agent system is modeled in a single large file. The file is then duplicated for each Lemma or invariant we wish to prove.

The four-agent system is split into many files containing multiple hybrid programs. These files specify the various interactions between pairs of agents (e.g. agent 1 receives 
information from agent 2, agent 3 receives information from agent 1, etc.). The folders are organized first by the Lemma/invariant, and then the pair of agents the lemma/invariant
is verified for. Only the files containing the necessary interaction between the pairs of agents specified by the invariant are used to verify the invariant. For example, if an 
invariant only concerns agents 1 and 2, then only the files detailing interactions with agent 1 or agent 2 will be used.

The files are named in the following structure: NumberOfAgents_Lemma_Invariant_AgentPair_Computation_Transmission_(PartNumber).
For example the file name "FourAgents_L4_inv7_a1a2_a1computea2_a1receivea3_part1" indicates that the file contains:

1. A four agent system
2. The invariant 7 for the pair of agents 1 and 2, used to prove Lemma 4 for agents 1 and 2
3. The specification for the timeslot (t, t+delta) when agent 1 computes it's estimated robustness based on information from agent 2, and then receives information from agent 3. 

The "part1" appended at the end of the filename indicates that the proof for the invariant is split into multiple parts, with the specific file containing part 1 of the proof.

# Reproducing Proofs

To reproduce a proof, simply copy the contents of a file into a new model in KeyMaera X and save. If the file contains a tactic, then clicking "Run stored tactic" will produce the proof
for that file. If a tactic is not included or if the prover stalls, then the proof can be manually reproduced following the guidance in the comment section at the head of the file. 

