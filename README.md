# Oracle-for-Shor
This repo contains my work in constructing an oracle for Shor's algorithm. The oracle is a function denoted $cU_a(a, N)$. The inputs $a$ and $N$ are positive integers with $a < N$, and the output is a (2n+3)-qubit quantum circuit that acts on the (n+1)-qubit quantum state $|x\rangle_1|y\rangle_n$ in the following way:
$$U|x\rangle_1|y\rangle_n = \begin{cases}
  |x\rangle_1|ay \mod N\rangle_n & \text{if }x=1\text{ and }y<N \\
  |x\rangle_1|ay \mod N\rangle_n & \text{otherwise.}
$$
Note in particular that since the circuit consists of 2n+3 qubits, the output will be a (2n+3)-qubit quantum state, however the n+2 most siginificant bits can be ignored; the n+1 least significant qubits will yield the output shown above. 
