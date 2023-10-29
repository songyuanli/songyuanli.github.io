---
layout: page
cover-img: 
  - "assets/img/research_wordcloud.jpg": "Research Keywords (as of November 2023)"
title: Research Overview
---

<a name="top"></a>

{% assign bib_file = 'simple.bib' %}

<style>
h3 {
	color: #007d69;
	margin-top: 0.7em;
	margin-bottom: 0.3em;
	padding-bottom: 0.2em;
	line-height: 1.0;
	padding-top: 0.5em;
	border-bottom: 1px solid #00dca5;
}

p {  
    line-height: 1.5;
    margin: 0;
    text-align: justify;
}
</style>

<strong><u>Shortcut to</u></strong><b>:</b><br>
<a href="/research">Research Overview</a> · <a href="/projects">Research Projects</a> · <a href="/publications">Publications</a> · <a href="/talks">Invited Talks</a> · <a href="/services">Professional Services</a>

<h3>Summary</h3>
<p>My research focus includes</p>
{::options parse_block_html="true" /}
- [Web Service Selection, Composition, and Recommendation](#web): QoS evaluation and optimization of workflows, Concurrent service selection based on service ecosystem
- [Cloud Resource Pricing, and Demand Allocation](#cloud): QoS awareness, Resource management, Task scheduling, Market-oriented cloud resource pricing strategy, Demand response
- [Fog Computing, and Mobile Edge Computing](#fog): QoS/QoE awareness, Edge resource management, Task routing & scheduling, Multi-user/service provider gaming, Efficient/Decentralized solution
- [Edge Intelligence, and Distributed Machine Learning](#edge_ai): Edge Intelligence, and Federated Learning: Synergistic DNN inference and training, Multi-exit DNN inference at edge, Edge-AI market design

<a name="web"></a> 
<h3>Web Service Selection, Composition, and Recommendation</h3>

The increasing momentum of service-oriented architecture has led to the emergence of divergent delivered services, where service selection is meritedly required to obtain the target service fulfilling the requirements from both users and service providers. I target to fill the research gap in the case where service requests from multiple users are performed simultaneously by a certain set of shared candidate services, although many existing works have extensively handled the issue of service selection. Meanwhile, I consider the constraints enforced on the context of service selection, such as, service placement location and contracts between users and service providers. In this sense, I propose a QoS-aware service selection scheme with constraints from a fairness aspect, with the objective of achieving max-min fairness across multiple service requests. In specific, I formulate this problem as a lexicographical maximization problem, which is yet far from trivial to deal with practically due to its inherently multi-objective and discrete nature. Given this, I develop an efficient fairness-aware algorithm for concurrent service selection, whose basic idea is to iteratively solve the single-objective subproblems by transforming them into linear programming problems. This work has been published in the IEEE ICWS 2019.

<br>
<div class="row col-sm-6" style="text-align: center;">
   <img src="{{ '/assets/img/service_selection.png' | relative_url }}" alt="Figure: Web Service Selection, Composition, and Recommendation"/>
</div>
<br>

<h4>Research Outputs:</h4>
<div class="publications" style="margin: 0;">
{% bibliography -f {{bib_file}} -q @*[doi=10.1109/ICWS.2019.00051]* %}
</div>

<figure>
 <a href="#top">
  <img src="../assets/img/top.png" alt="top" style="float: right;" width="30" height="30">
 </a>
</figure>
<br>

<a name="cloud"></a> 
<h3>Cloud Resource Pricing, and Demand Allocation</h3>

For a cloud service provider (CSP), it necessitates an emerging cloud ecosystem to both consolidate numerous cloud users and earn great revenue from users, further gaining its market share and achieving profitablity. Therefore, I design a price-incentive resource auction mechanism in cloud environment. In response to the cloud resource price, each user synthesizes her bidding budget and QoS requirement, and purchases cloud resources according to her resource demand in a strategic manner. The CSP, meanwhile, can regulate the resource demands of users through conducting a market-oriented pricing strategy, against too low prices to cover the operational costs or too high prices resulting in user churn. My proposed price-incentive resource auction mechanism targets to either maximize the CSP's service revenue, or stimulate maximum users willing to purchase cloud resources, on the premise of a minimum proﬁt rate guaranteed for the CSP. It is also expected to provide budge balance and truthfulness guarantee, and satisfy the envy-freeness. To carry out the above objectives, I define the user utility function reﬂecting the complicated user interest, and formulate our resource pricing and auction problem as a BP problem. Regarding the NP-hardness of optimization problem and the non-convexity of user utility, I present the counterpart computational-efﬁcient heuristic algorithm. The above work is presented in two research papers differentially standing in the place of cloud users or CSP, accepted for publication in the IEEE Transactions on Network and Service Management (TNSM).

<div class="row justify-content-md-center">
   <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/resource_pricing.png' | relative_url }}" alt="Figure: Cloud Resource Pricing, and Demand Allocation"/>
</div>
<br>

<h4>Research Outputs:</h4>
<div class="publications" style="margin: 0;">
{% bibliography -f {{bib_file}} -q @*[doi=10.1109/TNSM.2021.3085519]* %}
{% bibliography -f {{bib_file}} -q @*[doi=10.1109/TNSM.2020.3036989]* %}
</div>

<figure>
 <a href="#top">
  <img src="../assets/img/top.png" alt="top" style="float: right;" width="30" height="30">
 </a>
</figure>
<br>

<a name="fog"></a> 
<h3>Fog Computing, and Mobile Edge Computing</h3>

With the increasing prevalence of online services mounted on IoT devices, edge computing gains signiﬁcant momentum over conventional cloud-centric architecture. Edge servers are geographically deployed in a distributed manner nearby IoT devices, which not only frees online services from the high hardware requirement but also sharply reduces network latency experienced by end users. Given this, I study the QoS evaluation and optimization issues with regard to the edge scenario, specifically covering the following five aspects:
- Design queueing network models for QoS evaluation of IoT services in edge-cloud systems, published in the International Journal of Web and Grid Services (IJWGS).
- Conduct reliability-aware QoS evaluation for recoverable IoT edge services using the modeling techniques of generalized stochastic Petri net (GSPN), presented in the IEEE SCC 2017.
- Manipulate the MDP-based resource allocation and task scheduling in edge computing paradigm weighing energy costs against QoS requirements, presented in the IEEE ISPA 2017.
- Study the dynamic QoS-aware task scheduling and resource management problem in mobile edge computing by designing an efficient optimization algorithm with the effective and efficient LP relaxation techniques, published in the Peer-to-Peer Networking and Applications (PPNA).
- Adopt the potential game theory to solve the edge resource allocation problem with Quality of Experience (QoE) maximization in a decentralized manner, published in the IEEE Transactions on Cognitive Communications and Networking (TCCN).


<div class="row justify-content-md-center">
   <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/edge_computing.png' | relative_url }}" alt="Figure: Fog Computing, and Mobile Edge Computing"/>
</div>
<br>

<h4>Research Outputs:</h4>
<div class="publications" style="margin: 0;">
{% bibliography -f {{bib_file}} -q @*[doi=10.1109/TCCN.2021.3118460]* %}
{% bibliography -f {{bib_file}} -q @*[doi=10.1007/s12083-020-00880-y]* %}
{% bibliography -f {{bib_file}} -q @*[doi=10.1504/IJWGS.2018.090742]* %}
{% bibliography -f {{bib_file}} -q @*[doi=10.1109/ISPA/IUCC.2017.00129]* %}
{% bibliography -f {{bib_file}} -q @*[doi=10.1109/SCC.2017.70]* %}
</div>

<figure>
 <a href="#top">
  <img src="../assets/img/top.png" alt="top" style="float: right;" width="30" height="30">
 </a>
</figure>
<br>

<a name="edge_ai"></a> 
<h3>Edge Intelligence, and Distributed Machine Learning</h3>

The convergence of edge computing and artificial intelligence (AI) gives rise to Edge-AI, which enables the deployment of real-time AI applications and services at the network edge. One of the fundamental research issues in Edge-AI is edge inference acceleration, which aims to realize low-latency high-accuracy Deep Neural Network (DNN) inference and training services by leveraging the fine-grained offloading of partitioned DNN computation tasks from end devices to edge servers. However, the existing research has yet to take a more practical Edge-AI ecosystem perspective, which should consider not only the personalized performance requirements of AI users (e.g., DNN accuracy, runtime latency, and prediction task complexity), but also the incentives (e.g., revenue) for AI service providers offering edge inference services. To bridge this gap, I design the Auction-based Incentive Mechanism (AERIA) for edge inference and training tasks to tackle the multi-dimensional optimization problem of DNN model partition, edge inference pricing, and resource allocation. We investigate the device-edge synergistic inference/training scheme for on-demand DNN processing acceleration, and analyze the auction dynamics amongst the AI service provider, AI users and edge infrastructure provider. Owing to the strategic mechanism design, the Edge-AI ecosystem attains several desirable properties, including competitiveness in revenue maximization, incentive compatibility, and envy-freeness, which are crucial to maintain the effectiveness, truthfulness, and fairness of our multi-dimensional optimization outcomes. This work is considered for acceptance in the IEEE/ACM Transactions on Networking.

<br>

<div style="text-align: center;">
<img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/edge_ai.png' | relative_url }}" alt="Figure: Cloud Resource Pricing, and Demand Allocation"/>
</div>

<br>
<h4>Research Outputs:</h4>
<div class="publications" style="margin: 0;">
{% bibliography -f {{bib_file}} -q @*[doi=ToN]* %}
</div>

<figure>
 <a href="#top">
  <img src="../assets/img/top.png" alt="top" style="float: right;" width="30" height="30">
 </a>
</figure>
