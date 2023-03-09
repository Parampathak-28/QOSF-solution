# QOSF-solution
# this is the solution to the qosf task 1 2023. The question is to find the largest number among two numbers using a quantum algorithm.

# The algorithm for the solution is provided here.  

# step 1-->  encoding:-
# Let x0 be the integer to encode, then for any 1 digit in the binary representation of x0 you should apply an X gate to its corresponding qubit. E.g, let x0=11 (decimal value), then its binary representation is 1011, so then it can be encoded into 4 qubits as :
![xor gate output](https://user-images.githubusercontent.com/127308779/224099370-476edab7-f7c0-4ce1-b510-f406044f395d.png) 

# step 2--> Comparison:-

# We would compare qubit-by-qubit using a negated XOR operation into auxiliary qubits, followed by an MCX with all the auxiliary qubits as control qubits. The XOR operation writes |1⟩ to the auxiliary qubit when the 2 compared qubits are unequal, then by negating the auxiliary qubit we ensure that |1⟩ is written to the auxiliary qubit when the 2 compared qubits are equal in value. The XOR operation is implemented using a CNOT gate from each compared qubit to the auxliairy qubit. E.g when comparing 2 integers of 2-bits length each, it looks like this:  
![ckt img](https://user-images.githubusercontent.com/127308779/224100372-306c1e87-7c12-4fee-92b5-335cc7b99c16.png)

# If the numbers we feed in are equal( be it 00 or 11):
# |1⟩ would be written into the result qubit if and only if number_1 and number_2 are equal. 
