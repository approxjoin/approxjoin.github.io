---
layout: default
---

<div class="large-2 large-push-2 columns" markdown="0" style="text-align:center;">
        <a href="https://dl.acm.org">
            <img class="t0" width="60%" src="/images/acm-icon.png" alt="Paper">
            <div style="text-align:center; margin: 0 0 0 0; font-size: 0.8em;">Paper</div>
        </a>
</div>

<div class="large-2 large-push-2 columns" markdown="0" style="text-align:center;">
        <a href="https://arxiv.org/pdf/1805.05874.pdf">
            <img class="t0" width="60%" src="/images/report-icon.png" alt="Technical report">
            <div style="text-align:center; margin: 0 0 0 0; font-size: 0.8em;">Technical report</div>
        </a>
</div>    

<div class="large-2 large-push-2 columns" markdown="0" style="text-align:center;">
        <a href="/docs/bib.md">
            <img class="t0" width="60%" src="/images/bibtex-icon.png" alt="Bibtex">
            <div style="text-align:center; margin: 0 0 0 0; font-size: 0.8em;">BibTex</div>
        </a>   
</div>

<div class="large-2 large-push-2 columns" markdown="0" style="text-align:center;">
        <a href="https://github.com/approxjoin?tab=repositories">
            <img class="t0" width="60%" src="/images/github-icon.png" alt="Source code">
            <div style="text-align:center; margin: 0 0 0 0; font-size: 0.8em;">Source code</div>
        </a>
</div>

---

# Introduction
The join operation is a fundamental building block of parallel data processing. Unfortunately, it is very resource-intensive to compute an equi-join across massive datasets. The approximate computing paradigm allows users to trade accuracy and latency for expensive data processing operations. The equi-join operator is thus a natural candidate for optimization using approximation techniques.

<!-- <div align="center">
  <img style="text-align:center;" class="img-join" src="/images/join.png" alt="join" style="height: 150px; weight: 100px;"/>
</div> -->

Although sampling-based approaches are widely used for approximation, sampling over joins is a compelling but challenging task
regarding the output quality. Naive approaches, which perform joins over dataset samples, would not preserve statistical properties
of the join output.

<div align="center">
  <img style="text-align:center;" class="img-approxjoin" src="/images/approxjoin.jpg" alt="approxjoin" style="height: 250px; weight: 350px;"/>
</div>

To realize this potential, we interweave Bloom filter sketching and stratified sampling with the join computation in a new operator, ApproxJoin, that preserves the statistical properties of the join output. ApproxJoin leverages a Bloom filter to avoid shuffling non-joinable data items around the network and then applies stratified sampling to obtain a representative sample of the join output. Our analysis shows thatApproxJoin scales well and significantly reduces data movement, without sacrificing tight error bounds on the accuracy of the final results.

# Source Code
Source code will be available soon.
<!-- The source code of ApproxJoin is available <a href="https://github.com/approxjoin?tab=repositories"> here </a> -->
* Cluster deployment <a href="https://github.com/approxjoin/spark-setup"> script </a> 

------
# News
* This work has been accepted to ACM SoCC'18, see you in Carlsbad, California!


-------
