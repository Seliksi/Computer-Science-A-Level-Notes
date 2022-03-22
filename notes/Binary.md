### Binary
Binary is the base-2 numerical representation.
***
##### Simple binary representation
Let us consider the number $0010\;0110_{(2)}$.

128|64|32|16|8|4|2|1
-|-|-|-|-|-|-|-
0|0|1|0|0|1|1|0
As directed by the table above, the number $0010\;0110_{(2)}$ corresponds to the denary (base-10) number $32 + 4 + 2 = \boldsymbol{38}$. In general, if the $n$th from the LSB[^1] bit of a binary number is $1$, then it contributes $2^n$ to the value. This is what it means to be a 'base-2' number.
***
##### Simple binary arithmEtic (Addition)
At each iteration of the binary arithmetic process, there can be at most $1$s being summed together. The behaviour of these is as follows:
$$
\hspace{-10cm}
\begin{aligned}
	0 &\implies 0\\
	1 &\implies 1\\
	1 + 1 &\implies 0,\;carry\; 1\\
	1 + 1 + 1 &\implies 1,\;carry\;1
\end{aligned}
$$
To see how these rules apply in binary addition, consider this example, with accompanying denary annotations:
$$
\hspace{-10cm}
\begin{aligned}
	  &\;\; 00110110 \hspace{1.5em} = 54\\
	+ &\;\; 01110011 \hspace{1.5em} = 115\\
        &\hspace{-0.5cm}\textcolor{white}{\rule[0.5ex]{5.5em}{0.55pt}}\\
	  &\;\; 10101001 \hspace{1.5em} = 169\\
\end{aligned}
$$
Before subtraction can be introduced, binary representations which can describe negatives must first be described:
***
##### Negative Binary representation
There are two methods for representing negative numbers in binary: 'Sign and Magnitude' and 'Two's complement'.

When representing as **Sign and Magnitude**, one bit from the number (usually the most significant, aka first, bit) is used to denote the sign of the number, and the rest remain used for representing the value in a format identical to unsigned numbers. S & M has two major drawbacks:
- It is non-trivial to add two signed numbers represented this way - there have to be many exceptional considerations made, such as 

Under **Two's complement**, the MSB has its usual power-of-two value negated - for example, the MSB in an 8-bit number would have a positional value of $-128$, rather than $128$. The effect of this is 


[^1] Least Significant Bit