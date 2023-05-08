Download Link: https://assignmentchef.com/product/solved-s670-mini-project-2-new-version
<br>
The thinktank Data for Progress collected survey data (in DFP WTHH release.csv) that represents the population of people registered to vote in the 2018 midterm elections. We wish to study <strong>swing voters</strong>. Define the following groups:

<ul>

 <li><strong>Loyal Democrats: </strong>People who voted for Hillary Clinton in 2016 and a Democratic House candidate in 2018.</li>

 <li><strong>Loyal Republicans: </strong>People who voted for Donald Trump in 2016 and a Republican House candidate in 2018.</li>

 <li><strong>Swing voters: </strong>All other people who voted in 2018.</li>

</ul>

In addition, define the following two subsets of swing voters:

<ul>

 <li><strong>Switch to D: </strong>People who didn’t vote for Hillary Clinton in 2016 but voted for a Democratic House candidate in 2018.</li>

 <li><strong>Switch to R: </strong>People who didn’t vote for Donald Trump in 2016 but voted for a Republican House candidate in 2018.</li>

</ul>

Note that some swing voters don’t fall into either of these two groups, i.e. some people didn’t vote for either a Republican or a Democratic House candidate in 2018.

<h1>Basic variables</h1>

<ul>

 <li>presvote16post: 2016 Presidential election vote. 1 means Clinton, 2 means Trump, 3–7 or NA means voted for someone else or didn’t vote for President in 2016.</li>

 <li>house3: 2018 House of Representatives vote. 1 means Democrat, 2 means Republican, 3 means other.</li>

 <li>weight DFP: survey weights. You should use these!</li>

 <li>                                   Issue variables</li>

</ul>

Respondents were asked to give their support for the following programs on a 1–5 scale, where 1 means strongly support and 5 means strongly oppose. (6 means “Not sure.”)

<ul>

 <li>M4A: Medicare for All</li>

 <li>GREENJOB: A Green Jobs program</li>

 <li>WEALTH: A tax on wealth over $100 million</li>

 <li>MARLEG: Legalizing marijuana</li>

 <li>ICE: Defunding Immigration and Customs Enforcement</li>

 <li>GUNS: Gun control <a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a></li>

</ul>

The codebook (<a href="http://filesforprogress.org/datasets/wthh/WTHH_Core_and_DFP_modules.pdf">http://filesforprogress.org/datasets/wthh/WTHH_Core_and_DFP_modules</a>.

<a href="http://filesforprogress.org/datasets/wthh/WTHH_Core_and_DFP_modules.pdf">pdf</a><a href="http://filesforprogress.org/datasets/wthh/WTHH_Core_and_DFP_modules.pdf">)</a> contains full question wording for all issue variables.

<h1>Populism variables</h1>

Respondents were indicate their agreement with the following statements on a 1–5 scale, where 1

means strongly agree and 5 means strongly disagree. (6 means “Not sure.”)

<ul>

 <li>POP 1: “It doesn’t really matter who you vote for because the rich control both political parties.”</li>

 <li>POP2: “The system is stacked against people like me.”</li>

 <li>POP3: “I’d rather put my trust in the wisdom of ordinary people than in the opinions of experts and intellectuals.”</li>

</ul>

<h1>Questions to answer</h1>

First you need to create three subsets of the data: Switch to D voters, Switch to R voters, and Swing

Voters. The code in DFP.Rmd does this (creating data frames switchD, switchR, and swingers), or you might prefer to do it yourself. Then answer the following questions:

<ol>

 <li><strong>How do Switch to D and Switch to R voters differ on the issue variables?</strong></li>

</ol>

On which issue variables do Switch to D and Switch to R voters differ a lot? On which issue variables are they reasonably similar? Describe these differences.

<ol start="2">

 <li><strong>How do swing voters differ from loyal Democrats and loyal Republicans on the issue variables?</strong></li>

</ol>

Some hypotheses might be:

<ul>

 <li>Swing voters are moderates, and tend to the in the middle of the distribution when Democrats are on one side and Republicans are on the other.</li>

 <li>On most issues, swing voters are split, with some of them acting more like Democrats and others acting more like Republicans.</li>

 <li>Swing voters think more like Democrats on some issues and more like Republicans on other issues.</li>

 <li>Swing voters are ideologically incoherent and don’t have consistent patterns in their issue positions.</li>

</ul>

Which of these hypotheses (or which mixture of them) fits the data best, and for which issues?

<ol start="3">

 <li><strong>What predicts being a swing voter?</strong></li>

</ol>

Build two models to probabilistically predict whether a registered voter is a swing voter:

<ul>

 <li>One model should use ONLY the issue variables as predictors.</li>

 <li>The other model should use ONLY the populism variables as predictors.</li>

</ul>

Clearly display both models, showing how the predicted probability changes with each predictor you include.

How well do your models do? Which of your models does better? If you had to guess, what factors are most important in determining what makes a voter a swing voter?

Note: You don’t have to fit the best possible models, just sensible and interpretable ones. You should try to have some idea of how good your model is, although it may not be possible to improve classification error if nobody has a sufficiently high probability of being a swing voter.

<strong>Write a PDF report of no more than EIGHT pages, including graphs, addressing these questions. </strong>The body of the report should <em>not </em>include code — it should be readable to someone who has never used R (generally you should not just copy-paste output.) Additional graphs for model checking can be placed in an appendix that does not count toward the page limit and which probably no one will read.

<a href="#_ftnref1" name="_ftn1">[1]</a> The response choices were slightly different for this question; see the codebook.