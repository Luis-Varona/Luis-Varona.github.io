---
layout: page
title: Research
description: >
  Past, present, and future research directions.
---

1. TOC
{:toc}

This is an overview of my research in political science, computer science, mathematics, and economics, largely (but not entirely) conducted under the supervision of Drs. [Nathaniel Johnston](https://njohnston.ca/), [Craig Brett](https://mta.ca/directory/craig-brett), and [Wayne A. Hunt](https://mta.ca/directory/wayne-hunt) at Mount Allison University. Lately, I have mostly gravitated toward political science and CS (although essentially all CS research involves copious amounts of math), but my first few years of research as an undergrad centred almost exclusively around math and economics.

## Political Science

Although I am presently seeking to do graduate research in CS involving graph algorithms and/or graph structures, I would love to do research someday in computational social science (e.g., studying sociopolitical phenomena that arise on graph structures). In the meantime, most of my political science research has remained more qualitative (which is still enormously fun in its own way) as well.

### Technology & society
{:#technology-and-society}

This summer, I am researching the political philosophy of technology and society alongside Dr. Hunt. It constitutes only part-time work supplementing a grant I received for full-time CS research, but it has remained incredibly interesting nonetheless—it initially grew out of three essays I wrote for Dr. Hunt's full-year Political and Cultural Change seminar, which he proposed we synthesize into a paper with some additional political philosophy elements. Presently, we are writing up a draft tentatively entitled *Foundational models of sociopolitical change lag behind the ongoing reality of an algorithmic revolution*.

In particular, we are examining how foundational sociopolitical theories struggle to account for modern technology, which we argue is truly qualitatively different (not just faster or more efficient than prior forms) on a level that fundamentally changes how we live our lives. Among others, Herbert Marcuse (see *One-Dimensional Man*) and Antoinette Rouvroy (less well-known, but see her works on [algorithmic governmentality](https://doi.org/10.3917/res.177.0163)) are major philosophers with whom we engage. In this vein, we are also exploring how the emergent systems of [technofeudalism](https://www.penguin.co.uk/books/451795/technofeudalism-by-varoufakis-yanis/9781529926095) and [technofascism](https://doi.org/10.1007/s00146-026-02862-9) diverge from Karl Marx's traditional conceptions of the capitalist base and superstructure, and the ramifications of this for Marx's immanent conditions for revolution as people's agency diminishes.

---

## Computer Science

Most of my research energy as of late has been dedicated to CS, which I intend to continue pursuing in my graduate studies. The majority of my CS research revolves, in one form or another, around a graph invariant called [bandwidth](https://mathworld.wolfram.com/GraphBandwidth.html), which measures how far apart adjacent nodes must sit in the best possible node ordering. (If thinking about adjacency matrices instead, bandwidth measures the furthest distance of a nonzero entry from the diagonal under an optimal symmetric permutation.) Thus far, I have investigated graph bandwidth in the contexts of combinatorial graph algorithms and graph structure in neural networks. Lately, I have also been vaguely interested in bandwidth as it shows up in parameterized complexity (e.g., when computing metric dimension) and numerical analysis (factorizations of banded matrices, to be specific), but neither of those directions has yet produced anything concrete of which to speak.

### Graph algorithms

In Summer 2025, motivated by some vague applications to my then-supervisor's research in quantum information theory, I started developing a [Julia package](https://luis-varona.github.io/MatrixBandwidth.jl/) for bandwidth reduction algorithms (which has since been [published](https://doi.org/10.21105/joss.09136) in the *Journal of Open Source Software*). This entailed immersing myself in the relevant literature, and I was intrigued enough by the general topic of graph bandwidth to independently pursue a research inquiry into improving bandwidth algorithms throughout the Fall term and parts of Winter. (As a brief aside—between this and my other [independent graph theory project](#spectral-graph-theory) with another undergrad last year, I admit to spending less time on my undergraduate thesis than I perhaps should have. I ended up rushing through my entire thesis writeup in a span of three weeks, although I still did quite well—I am intimately familiar with such intense periods of writing as a Political Science major.)

This culminated in me posting a [preprint on the arXiv](https://doi.org/10.48550/arXiv.2602.01755) (currently under review at *Discrete Applied Mathematics*) in the Winter term, presenting an improved algorithm for recognizing graphs with high bandwidth. I am also entertaining the possibility of adapting unweighted heuristic methods (see the well-known [Cuthill–McKee algorithm](https://doi.org/10.1145/800195.805928)) to work better on weighted graphs; I am slated to give a short lightning talk on this line of inquiry at the 2026 East Coast Combinatorics Conference in July.

### Neural network theory

My main research project this summer, funded by an independent student research grant advised by Dr. Johnston, investigates training dynamics of recurrent neural networks (RNNs) whose weight matrices have bounded bandwidth. (This utilizes the matrix-theoretic interpretation of bandwidth, as we treat the weight matrix of an RNN as the adjacency matrix of a directed graph.) Bandwidth controls how far information can propagate through the hidden state per timestep; this allows one to mathematically predict at which tasks bandwidth-constrained RNNs excel and on which they underperform. I am, therefore, using formal language classification and modelling tasks (mostly regular languages, but with copying thrown in as well) to test such predictions.

This idea originated with [Dr. Marco Cognetta](https://mcognetta.github.io/) of Google—an informal mentor on the project—although it has since evolved considerably from his initial research proposal. The project is nearly done; I am hoping to have a preprint up on the arXiv by July, with the working title *Formal language learning in bandwidth-constrained recurrent neural networks*.

---

## Mathematics

Math was the first subject in which I conducted undergraduate research, and it remains a field which, as a prospective CS graduate student, I fully expect to continue utilizing heavily. Dr. Johnston, my first (and most frequent) research supervisor, primarily studies quantum information theory through the lens of linear algebra and spectral graph theory—these areas are where I, too, started my research career.

### Abstract linear algebra

My very first research project back in Summer 2024 was with Dr. Johnston, [Dr. Sarah Plosker](https://people.brandonu.ca/ploskers/) of Brandon University, and my friend Charles Torrance (who just recently graduated from Mount A!). This remains the most "pure math-y" of my projects to date, and by a considerable margin at that—we explored several Cauchy–Schwarz-type bounds tightening and/or generalizing the original inequality. (This is, loosely, connected to Drs. Johnston and Plosker's main research focus of quantum information theory via applications to separability of states.) Our paper, currently under journal review, is available as [a preprint on the arXiv](https://doi.org/10.48550/arXiv.2507.10327).

### Spectral graph theory

I am also currently collaborating (again!) with Drs. Johnston and Plosker on a spectral graph theory project, although it has taken a backseat to my other (actually funded) research endeavours this summer. In particular, we are wrapping up a long-running project we started (and temporarily abandoned) a few years ago—characterizing two classes of graphs known as Laplacian integral and $$\{-1,0,1\}$$-diagonalizable. While I have, in tandem with the two professors, proven several pure mathematical results, much of my contribution has taken a more computational bent. Most of my time working on this paper involved running computational surveys of these types of graphs and designing efficient algorithms to do so at scales well beyond what was previously feasible. We hope to have something out by July.

In Fall 2025, I also worked with fellow undergraduate student Finn Steinke over at Guelph (whom I met through one of my competitive programming teammates at Mount A) to derive efficiently computable spectral bounds on the chromatic number of powers of vertex-transitive graphs. To be clear, this project was Finn's brainchild; I, for the most part, simply helped fill in some gaps and write it up in paper form. (He and I have since [posted it on the arXiv](https://doi.org/10.48550/arXiv.2601.01962) and submitted it to an undergraduate math journal—nothing super fancy, but a venue well-suited to the paper, I hope.)

My undergraduate thesis (completed in my penultimate year, since I am taking five years to complete my degree) similarly involved spectral properties of graphs, applying optimization algorithms to model quantum walks on graphs. Somewhat unusually, I picked a thesis topic unrelated to anything I seriously entertained pursuing further (partially because my honours is in math instead of CS or political science, and partially because Dr. Johnston—who supervised me—has different research interests from mine), but I thoroughly enjoyed the research all the same. (Another friend of mine is currently working with Dr. Johnston to build on my results and hopefully end up with a paper, but I am only minimally involved with that particular project.)

---

## Economics

My research identity in economics is not quite as well-formed as in my three other disciplines, but so far, I have dealt largely with the field of microeconomics (specifically public finance, as Dr. Brett's research specialty).

### Public finance

In Winter 2025, I took a fourth-year Applied Econometrics course with Dr. Brett, who was looking into issues relating to policing expenditure in the province at the behest of the Union of Municipalities of New Brunswick. I chose to pursue this thread for my capstone project, and he hired me in the Fall to continue researching the topic with him (this was my first time doing academic research outside of math/CS!). More specifically, we investigated how exogenous municipal spending (such as policing bills set by the province) affects tax rates. Although I am no longer officially working with Dr. Brett this summer, we are currently attempting to wrap up the project and send the paper out for journal review.
