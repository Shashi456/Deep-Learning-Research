# The curious case of neural text degeneration
- Maximization based decoding approaches lead to degeneration (text of sub-par quality). 
- This paper suggests a new sampling method called Nucleus Sampling, it avoid degeneration by truncating the unreliable tail of the probability distribution, sampling from the dynamic nucleus of tokens. 
- Instead of relying on a fixed top-k, or using a temperature parameter to control the shape of the distribution without sufficiently suppressing the unreliable tail, the paper proposes sampling from the top-p portion of the probability mass.
- Open ended generation includes conditioanl story generation and contextual text continuation. This technique is one which would be helpful in that case. 
- The task of open ended generation is to generate text that forms a coherent continuation from the given context. 
- Maximization based decoding assigns higher probability to higher quality text, they try to maximize likelihood. Since the optimal sequence is not tractable, beam search is used.
- Nucleus Sampling's Key idea is to use the shape of the probability distribution to determine the set of tokens to be sampled from. In practise it means selecting high probability tokens whose cumulative probability mass exceeds the pre chosen threshold P.