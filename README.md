# Detection_of_Malicious_URLs_using_Lexical_features

## Problem Statement

<!-- wp:paragraph -->
<p>In this case study, we address the detection of malicious URLs as a multi-class classification problem. In this case study, we classify the raw URLs into different class types such as benign or safe URL, phishing URL, malware URL, or defacement URL. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>As we know machine learning algorithms only support numeric inputs so we will create lexical numeric features from input URLs. So the input to machine learning algorithms will be the numeric lexical features rather than actual raw URLs. If you don't know about lexical features you can refer to <a href="https://stackoverflow.com/questions/33282094/differences-between-lexical-features-and-orthographic-features-in-nlp" target="_blank" aria-label="undefined (opens in a new tab)" rel="noreferrer noopener nofollow">this </a>discussion about a lexical feature in StackOverflow.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>So, in this case study, we will be using three well-known boosting machine learning classifiers namely <strong>XGBoost</strong>, <strong>Light GBM</strong>, <strong>Gradient Boosting Machines</strong>. </p>
<!-- /wp:paragraph -->

## About Data

For training and testing machine learning algorithms, we have used a huge dataset of 651,191 URLs, out of which 428103 benign or safe URLs, 96457 defacement URLs, 94111 phishing URLs, and 32520 malware URLs. Figure 2 depicts their distribution in terms of percentage.
As we know one of the most crucial tasks is to curate the dataset for a machine learning project. We have curated this dataset from five different sources.

For collecting benign, phishing, malware and defacement URLs we have used [URL dataset (ISCX-URL-2016)](https://www.unb.ca/cic/datasets/url-2016.html)
For increasing phishing and malware URLs, we have used [Malware domain black list dataset](http://www.malwaredomains.com/wordpress/?page_id=66).
We have increased benign URLs using [faizan git repo](https://github.com/faizann24/Using-machine-learning-to-detect-malicious-URLs/tree/master/data)
At last, we have increased more number of phishing URLs using [Phishtank dataset](https://www.phishtank.com/developer_info.php) and [PhishStorm dataset](https://research.aalto.fi/en/datasets/phishstorm--phishing--legitimate-url-dataset(f49465b2-c68a-4182-9171-075f0ed797d5).html)
As we have told you that dataset is collected from different sources. So firstly, we have collected the URLs from different sources into separate dataframe and finally merge them to retain only URLs and their class type.

The final pre-processed dataset is available at kaggle https://www.kaggle.com/sid321axn/malicious

