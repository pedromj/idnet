Machine Learning in Networking
------------------------------

I thought I'd try to get some discussion going by outlining some of my views as to why networking is lagging other areas in the development and application of Machine Learning (ML). In particular, networking is way behind what we might call the "perceptual tasks" (vision, NLP, robotics, etc) as well as other areas (medicine, finance, ...). The attached slide from one of my decks tries to summarize the situation, but I'll give a bit of an outline below.

So why is networking lagging many other fields when it comes to the application of machine learning? There are several reasons which I'll try to outline here (I was fortunate enough to discuss this with the packetpushers crew a few weeks ago, see [0]). These are in no particular order.

First, we don't have a "useful" theory of networking (UTON). One way to think about what such a theory would look like is by analogy to what we see with the success of convolutional neural networks (CNNs) not only for vision but now for many other tasks. In that case there is a theory of how vision works, built up from concepts like receptive fields, shared weights, simple and complex cells, etc. For example, the input layer of a CNN isn't fully connected; rather connections reflect the receptive field of the input layer, which is in a way that is "inspired" by biological vision (being very careful with "biological inspiration"). Same with the alternation of convolutional and pooling layers; these loosely model the alternation of simple and complex cells in the primary visual cortex (V1), the secondary visual cortex(V2) and the Brodmann area (V3). BTW, such a theory seems to be required for transfer learning [1], which we'll need if we don't want every network to be analyzed in an ad-hoc, one-off style (like we see today).

The second thing that we need to think about is publicly available standardized data sets. Examples here include MNIST, ImageNet, and many others. The result of having these data sets has been the steady ratcheting down of error rates on tasks such as object and scene recognition, NLP, and others to super-human levels. Suffice it to say we have nothing like these data sets for networking. Networking data sets today are largely proprietary, and because there is no UTON, there is no real way to compare results between them.

Third, there is a large skill set gap. Network engineers (us!) typically don't have the mathematical background required to build effective machine learning at scale. See [2] for an outline of some of the mathematical skills that are essential for effective ML. There is a lot more to this, involving how progress is made in ML (open data, open source, open models, in general open science and associated communities, see e.g., OpenAi [3], Distill [4], and many others). In any event we need build community and gain new skills if we want to be able to develop and apply state of the art machine learning algorithms to network data, at scale. The bottom line is that it will be difficult if not impossible to be effective in the ML space if we ourselves don't understand how it works and further, if we can build explainable systems (noting that explaining what the individual neurons in a deep neural network are doing is notoriously difficult; that said much progress is being made). So we want to build explainable, end-to-end trained systems, and to accomplish this we ourselves need to understand how these algorithms work, but in training and in inference.

This email is already TL;DR but I'll add one more here: We need to learn control, not just prediction. Since we live in an inherently adversarial environment we need to take advantage of Reinforcement Learning as well as the various attacks being formulated against ML; [5] gives one interesting example of attacks against policy networks using adversarial examples. See also slides 31 and 32 of [6] for some more on this topic.

I hope some of this gets us thinking about the problems we need to solve in order to be successful in the ML space. There's plenty more of this on [7] and [8]. I'm looking forward to the discussion.

[0] http://packetpushers.net/podcast/podcasts/pq-show-107-applicability-machine-learning-networking<br/>
[1] http://sebastianruder.com/transfer-learning/index.html<br/>
[2] http://datascience.ibm.com/blog/the-mathematics-of-machine-learning<br/>
[3] https://openai.com/blog<br/>
[4] http://distill.pub<br/>
[5] http://rll.berkeley.edu/adversarial/arXiv2017_AdversarialAttacks.pdf<br/>
[6] http://www.1-4-5.net/~dmm/ml/talks/2016/cor_ml4networking.pptx<br/>
[7] http://www.1-4-5.net/~dmm/ml<br/>
[8] http://www.1-4-5.net/~dmm/vita.html<br/>
