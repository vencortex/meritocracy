# Meritocracy in Hybrid Intelligence Systems
Our team at [Darwin](https://www.askdarwin.com) pursues a vision of a hybrid approach for solving complex problems, powered by the human mind, augmented by machines. Indeed so-called human-in-the-loop machine learning plays an important role in the progress of machine learning models in both research and big tech giants such as Amazon or Google. In this case, human (experts) are used for teaching machine learning models. Probably the easiest and most common example for this is using crowdsourcing for image recognition i.e. ask people to identify what they see in an image. This data can then be used as labeled data to train a neural network that can discriminate between, let's say, a cat and a dog.

Although this task seems trivial, the quality of labeling is central to the success of a machine learning model. Therefore, data scientists try to come up with ways to measure human expertise. The relevance for such expertise becomes even more relevant when considering highly critical tasks such as labeling a CT scan if there are visible maligned nodes that might indicate cancer.

## Strategies for Identifying Experts
So how can you identify if the expert labeling the data is really an expert? Machine learning researchers have come up with some solutions which are unfortunately not applicable for complex problems in a real-world application.
- Probably the most straightforward approach, is comparing the experts' answers with the true label and seeing how often it was labeled correctly. However, this assumes that we already know the right answer. 
- Consensus labeling is another widely used method wherein, the agreement of an expert with other users is used as the measure of an expert's credibility. However, this approach also has significant flaws when it comes to complex and uncertain decisions. In such problems, the correlation between majority opinion and the "correct" answer is not reliable. While consensus might indicate expertise, it might also be a sign for systematic biases among a certain group of people or the result of so called herding effects that frequently lead to disastrous effects on financial markets.
- A third, frequently applied mechanism in Machine Learning tasks, is self-assessed confidence. This measure indicates how strongly an expert believes that her answer is correct. Once again this works relatively good for simple tasks and novices, but it frequently fails when the uncertainty and complexity of the problem grow and personal reputation is at stake. Such overconfidence might not be an issue as long as the expert is always right. However, it creates huge problems when confidence and actual performance are not well calibrated i.e. experts are wrong but yet confident in their decisions. Many studies from medicine to political decision making and venture capital highlight this issue.

## Meritocratic Human Input for Machine Learning Tasks
In the absense of a well-fitting expert credibility assessment model, our team set out to engineer a solution on top of the existing work from interdisciplinary fields.
*A meritocratic reputation score follows the notion that the status of an expert should be vested in individuals on the basis of talent, effort, and achievement, rather than factors such as sexuality, race,  gender, age, experience or wealth.*
For the application in hybrid systems that means users need to prove their talent to be called and used as an expert. In human in the loop machine learning, we divide meritocracy into two dimensions on-system and off-system meritocracy. While the first focus on meritocracy proven during the use of an AI system (for instance by providing labels), the latter is based on previous merits earned by a human expert (for instance achievements shown by her CV) and can be thus used as a prior. Although, such seniority in experience might not always be the best indicator (there are plenty of studies in medicine that show that highly experienced medical specialists don't outperform younger novices), it gives us at least some warm start.

While this sounds kind of ideologically driven in the first place, meritocracy for Hybrid Intelligence Systems is a very practical problem and researchers from psychology to weather forecasting are trying to come up with ideas to measure expertise empirically.

## The Darwin Formula
Based on our research true expertise or meritocracy, has seven major components.

**(1)** The first component is the **decision context**. That we distinguish between being an expert for identifying dogs vs being an expert for cats. A expert therefore has many meritocracies score, each of which depends on the context of the decision.

**(2)** Related to this context is the level of **uncertainty**. That means we distinguish between an expert providing wrong answers for difficult tasks vs an expert being wrong in easy decisions.

**(3)Reliability**  is a measure that combines the *validity* of an expert (how often she is correctly identifying a cat as a cat on an image) with her meta-cognitive ability of *calibration* (how confident she was in making right decisions vs wrong decisions). The problem with this measure is that typically the true outcome can be seen only in the future thus providing time delayed feedback and allowing to measure expertise just retrospectivly.

**(4)** The fourth important factor is *time*. Especially, in a dynamic world. While an expert for identifying dogs today will probably still be an expert 10 years from now, this is not necessarily true for other settings. Imagine for instance people assessing new technology or markets. The knowledge they proved to have some time ago is probably outdated today and requires the expert to continuously learn new things.

**(5)** However, time plays also another role that counts for the expert. We call this **explorative capacity**, meaning that people that were the first to provide an answer long ago before the true outcomes emerge prove higher level of expertise.

**(6)** **Discrimination** is the ability to respond differently to different stimuli. This means that although we might not know if somebody is right or wrong, expertise is proven when the expert reacts differently to different data points. This can be measured at any point in time without requiring the true outcome.

**(7)** The final component that can also be measured without knowing the true outcome is **consistency**. However, a high level of consistency can also be obtained if an expert is following a simple, but incorrect, rule, when followed precisely. Consistency can therefore be seen as a necessary but not sufficient criteria to determine expertise. This findings led to the development of one of the greatest formulas in empirical psychology of all time, [Cochran-Weiss-Shanteau (CWS)index](http://www.academia.edu/download/7579786/hfpublication03.pdf), defined as

![GitHub Logo](http://www.w3.org/1999/xlink)


Based on those parts we are finally building the Darwin formula for meritocracy, which is a combination of the ingredients:
\\[ display \\]DarwinMeritocracy_{expert_{i}}(x_{i}, t) = \frac{CAPACITY_{explorative}(x_{i},t)}{RELIABILITY-RESOLUTION+UNCERTAINTY(x_{i})}*\frac{DISCRIMINATION(Expert\mid x_{i})}{INCONSISTENCY(Expert\mid x_{i})}*\frac{1}{(1+r)^{t}}\\[ display \\]

We use this generic formula for assessing meritocratic expertise in our hybrid intelligence systems for judgement and prediction tasks. If you are interested in more details or an algorithmic implementation of this formula follow support us working on this formula.
