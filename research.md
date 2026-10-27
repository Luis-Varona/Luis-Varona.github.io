---
layout: page
title: Research
description: >
  Past, present, and future research directions.
---

1. TOC
{:toc}

This is an overview of my research in political science, computer science, economics, and mathematics, largely (but not entirely) conducted under the supervision of Drs. [Nathaniel Johnston](https://njohnston.ca/), [Craig Brett](https://mta.ca/directory/craig-brett), [Wayne A. Hunt](https://mta.ca/directory/wayne-hunt), and [Liam Keliher](https://mta.ca/directory/liam-keliher) at Mount Allison University. Lately, I have mostly gravitated toward political science and CS (still, essentially all CS research involves copious amounts of math), but my first few years of research as an undergrad centred almost exclusively around economics and math.

## Political Science

Although I am presently seeking to do graduate research in CS, I would love to do research someday in computational social science (e.g., studying sociopolitical phenomena that arise on graph structures). I am also interested in finding graduate supervisors whose graph-related work involves public policy or economics in some way. In the meantime, my political science research thus far has remained more on the qualitative end of things.

### Technology & society
{:#technology-and-society}

In Summer 2026, I researched the political philosophy of technology and society alongside Dr. Hunt. It constituted only part-time work supplementing a grant I received for full-time CS research, but it was incredibly interesting nonetheless—it initially grew out of three essays I wrote for Dr. Hunt's full-year Political & Cultural Change seminar, which he proposed we synthesize into a paper with some additional political philosophy elements. Presently, we are writing up a draft tentatively entitled *Indispensable: The digital capitalist class and Gramscian conditions of revolution*. We are hoping to eventually turn it into a book as well.

In particular, we argue that a new "digital capitalist class" consisting of Big Tech firms has arisen, whose control of technological infrastructure has made it indispensable to both the state and society. Using a class-theoretic framework, we study how this has eroded the Marxist and Gramscian conditions of revolution across the interconnected domains of personal privacy, institutional governance, national security, and civil society, as well as how to rebuild these conditions. We also draw on theoretical frameworks such as Rouvroy and Berns's algorithmic governmentality, Couldry and Mejias's data colonialism, Giblin and Doctorow's chokepoint capitalism, and more to develop this argument.

---

## Computer Science

Most of my research energy as of late has been dedicated to CS, which I intend to continue pursuing in my graduate studies. The majority of my CS research revolves, in one form or another, around a graph invariant called [bandwidth](https://mathworld.wolfram.com/GraphBandwidth.html), which measures how far apart adjacent nodes must sit in the best possible node ordering. (If thinking about adjacency matrices instead, bandwidth measures the furthest distance of a nonzero entry from the diagonal under an optimal symmetric permutation.) Thus far, I have investigated graph bandwidth in the contexts of combinatorial graph algorithms and graph structure in neural networks. Lately, I have also been vaguely interested in bandwidth as it shows up in parameterized complexity (e.g., when computing metric dimension) and numerical analysis (factorizations of banded matrices, to be specific), but neither of those directions has yet produced anything concrete of which to speak.

### Graph algorithms

In Summer 2025, motivated by some vague applications to my then-supervisor's research in quantum information theory, I started developing a [Julia package](https://luis-varona.github.io/MatrixBandwidth.jl/) for bandwidth reduction algorithms (which has since been [published](https://doi.org/10.21105/joss.09136) in the *Journal of Open Source Software*). This entailed immersing myself in the relevant literature, and I was intrigued enough by the general topic of graph bandwidth to independently pursue a research inquiry into improving bandwidth algorithms throughout the Fall term and parts of Winter. This culminated in me posting a [preprint on the arXiv](https://doi.org/10.48550/arXiv.2602.01755) (currently being revised for a v2 preprint and journal submission) in the Winter term, presenting an improved algorithm for recognizing graphs with high bandwidth.

More recently, I have been collaborating with Dr. Keliher and Alexander Matheson (his CS honours student at MtA, and a friend of mine) to generalize heuristic and metaheuristic bandwidth reduction algorithms (see, e.g., the well-known [Cuthill–McKee algorithm](https://doi.org/10.1145/800195.805928)) to weighted graphs. (In July 2026, I gave a [short lightning talk](/assets/slides/eccc-2026.pdf) on this topic at the [19<sup>th</sup> East Coast Combinatorics Conference](https://www.aarms.math.ca/events/east-coast-combinatorics-conference).) I am currently working as a research assistant while Alex does his honours thesis on the same topic, and the three of us intend to write a paper together—probably focusing more on heuristics than metaheuristics—sometime in the next year or two.

### Neural network theory

My main research project in the Summer 2026 term, funded by an independent student research grant advised by Dr. Johnston, investigated training dynamics of recurrent neural networks (RNNs) whose weight matrices have bounded bandwidth. (This utilizes the matrix-theoretic interpretation of bandwidth, as we treat the weight matrix of an RNN as the adjacency matrix of a directed graph.) Bandwidth controls how far information can propagate through the hidden state per timestep; this allows one to mathematically predict at which tasks bandwidth-constrained RNNs excel and on which they underperform. Therefore, I used formal language classification and modelling tasks (mostly regular languages, but with copying thrown in as well) to test such predictions.

This idea originated with [Dr. Marco Cognetta](https://mcognetta.github.io/) of Google—thus far an informal mentor of sorts on the project—although it has since evolved considerably from his initial research proposal. Although the summer proved an inadequate period to finish the project, I plan to resume research sometime in the coming months.

---

## Economics

My research in economics thus far encompasses two projects in strikingly different subfields, both supervised by Dr. Brett—network formation games and municipal public finance. Looking forward, I am interested in graduate CS supervisors whose work connects to economics via social network analysis, game theory, or simulation-based models, as the field lies squarely at the intersection of quantitative analysis and public policy.

### Network analysis

I am currently researching a class of graph structures known as communication networks with Dr. Brett. These are graphs whose edges are formed by self-interested agents associated with each node seeking to derive value from other nearby agents, with this payoff decaying exponentially as shortest-path distance increases. Our particular contribution to the field involves bounding the degree of each node and investigating how this affects the efficient and Nash structures that arise during network formation. We hope to finish a paper, *Unilateral link formation in degree-constrained communication networks*, by the end of the Fall 2026 term. (In the meantime, the [slides](/assets/slides/mscs-2026.pdf) from my October 2026 talk at the [2026 Science Atlantic MSCS Conference](https://event.fourwaves.com/mscs2026) offer a nice overview of our project.)

### Public finance

In Winter 2025, I took a fourth-year Applied Econometrics course with Dr. Brett, who was looking into issues relating to policing expenditure in the province at the behest of the Union of Municipalities of New Brunswick. I chose to pursue this thread for my capstone project, and he hired me in the Fall 2025 term to continue researching the topic with him (this was my first time doing academic research outside of math/CS!). More specifically, we investigated how exogenous municipal spending (such as policing bills set by the province) affects tax rates. Having wrapped up some remaining loose ends in Summer 2026, we are almost ready to conclude writing and submit our paper to a public policy journal, once we resume in Summer 2027.

---

## Mathematics

Math was the first subject in which I conducted undergraduate research, and it remains a field which, as a prospective CS graduate student, I fully expect to continue utilizing heavily. Dr. Johnston, my first research supervisor, primarily studies quantum information theory through the lens of linear algebra and spectral graph theory. These areas are where I, too, started my research career, although I have long since moved away from them.

### Spectral graph theory

I spent the 2025–26 school year (along with bits of free time throughout the Summer 2026 term) working with Dr. Johnston and [Dr. Sarah Plosker](https://people.brandonu.ca/ploskers/) of Brandon University on a spectral graph theory paper, out now as [a preprint on the arXiv](https://doi.org/10.48550/arXiv.2607.06336) (and currently under peer review). We characterized two classes of graphs known as Laplacian integral and $$\{-1,0,1\}$$-diagonalizable, as well as produced extensive computational results on a large number of specific cases. While I did prove some pure mathematical results in tandem with the two professors, most of my contribution to this paper took a more computational bent—in particular, I ran computational surveys of these types of graphs and designed efficient algorithms to do so at scales well beyond what was previously feasible.

In Fall 2025, I also worked with fellow undergraduate student Finn Steinke over at Guelph (whom I met through one of my competitive programming teammates at MtA) to derive efficiently computable spectral bounds on the chromatic number of powers of vertex-transitive graphs. To be clear, this project was Finn's brainchild; I, for the most part, simply helped fill in some gaps and write it up in paper form. (He and I have since [posted it on the arXiv](https://doi.org/10.48550/arXiv.2601.01962) and submitted it to an undergraduate math journal—nothing super fancy, but a venue well-suited to the paper, I hope.)

My undergraduate thesis (completed in my penultimate year, since I am taking five years to complete my degree) similarly involved spectral properties of graphs, applying optimization algorithms to model quantum walks on graphs. (This was more of a fun little tangent than anything else, irrelevant to my actual research interests—even when writing my thesis, I never really planned to pursue the topic any further.)

### Abstract linear algebra

My very first research project (across any discipline) back in Summer 2024 was with Dr. Johnston, Dr. Plosker, and my friend Charles Torrance (a recent graduate from MtA). This remains the most "pure math-y" of my projects to date, and by a considerable margin at that—we explored several Cauchy–Schwarz-type bounds tightening and/or generalizing the original inequality. (This is, loosely, connected to Drs. Johnston and Plosker's main research focus of quantum information theory via applications to separability of states.) Our paper has since been [published](https://doi.org/10.1080/03081087.2026.2707240) in *Linear and Multilinear Algebra*.
