Reinforcement Learning: Basic Information
-----------------------------------------

Totally agree we need to learn from our environment, and RL is a natural approach. After all, the network is always changing, has adversaries, etc. All of this means. among other things, that we can't make simplifying assumptions like stationary distributions,  iid data, .... So RL is one way to attack these problems, and the classic algorithms you mention below are certainly a reasonable approach (I've been working with policy gradients [0], trying to model/adapt the two-player game approach of AlphaGo to networking; the problem there is that we don't have a source of labeled expert data like the KGS Go server [7] to build the supervised policy network....).

You might also want to check out the recent "boot" of evolution strategies as a black-box approach to RL (in particular no gradients). See [1],  [2], [3]. There is also a ton of code around if you want to try some of this out (find one in tensorflow in [6]). Finally, I've attached a few summary slides with some of my musings on this topic from past talks.

BTW, two player minimax games seem to be popping up everywhere: AlphaGo, variational autoencoders [4], GANs [5], and many others; something to thing about for our domain.

[0] https://papers.nips.cc/paper/1713-policy-gradient-methods-for-reinforcement-learning-with-function-approximation.pdf<br/>
[1] https://blog.openai.com/evolution-strategies/<br/>
[2] https://arxiv.org/pdf/1703.03864.pdf<br/>
[3] http://jmlr.csail.mit.edu/papers/volume15/wierstra14a/wierstra14a.pdf<br/>
[4] http://www.1-4-5.net/~dmm/ml/vae.pdf<br/>
[5] https://arxiv.org/pdf/1406.2661.pdf<br/>
[6] https://github.com/dennybritz/reinforcement-learning<br/>
[7] https://www.gokgs.com/<br/>
