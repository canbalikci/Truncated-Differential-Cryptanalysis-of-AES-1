# ToSC-june-2026-Truncated-Differential-Attack-on-AES

For Proposition 1; 
Before running this code, adjust a random permutation value in the "double compute_divisor()" section according to your desired j using the formula from Remark 1 in the paper.

For Theorem 1;
Before running this code, adjust a random permutation value in the "double compute_divisor()" section according to your desired j using the formula from Remark 1 in the paper.

For Theorem 2;
Using the code in this section, you can compute the values of $P^6_{m,2}$ for your chosen m values. Then, using the code in the Corollary 1 file, find the corresponding $Pr[m\rightarrow _6 3]$ ratio for the same m values. Finally, apply the formula given in Theorem 2 to calculate $Pr[m\rightarrow _6 2]$ for each m. 

For Number of Path;
This code implements one round consisting of MC and SR operations. An n-round encryption therefore consists of n MC operations and n + 1 SR operations. You can specify which bytes are active in the input by editing the line "static state_t in = { .active = {0} }". Similarly, you set the desired number of active bytes in each output column by changing "int target_counts[NCOLS] = {3, 3, 4, 4};". In this way, for any input configuration and after n + 1 rounds of SR (i.e. just before the (n + 1)th MC), the program will count all possible propagation paths that match the specified active-byte patterns.
