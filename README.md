# My solution to the Lights out puzzle in week 2A of the IBMQ challenge
From November 7 to November 28, IBM hosted a quantum challenge that included 5 execises spread over the three week period. This was the solution that I came up with 
for the third exercise where we were tasked with creating a quantum algorithm to solve any 3x3 board configuration of the famous lights out puzzle.  

The approach I took:
1. Apply hadamard transform of the flip qubits
2. Initialize board state on the tile qubits
2. X + H to the oracle qubit
3. Connect all flip qubits to tile qubits following the implications of flipping on/off a certain block
4. Kicking a negative phase to the board config with all 0 lights
5. Kicking that negative phase back up to the flip qubit config that resulted in that all zero config
6. Applying the diffusion operator to the flip qubits to amplify probabilities of measuring the solution.
7. After enough iterations, measure the solution.
