---
title: "Key challenges for delivering clinical impact with artificial intelligence"
source: "https://link.springer.com/article/10.1186/s12916-019-1426-2"
author:
  - "[[Christopher J. Kelly]]"
  - "[[Alan Karthikesalingam]]"
  - "[[Mustafa Suleyman]]"
  - "[[Greg Corrado]]"
  - "[[Dominic King]]"
published: 2019-10-29
created: 2026-06-27
description: "Artificial intelligence (AI) research in healthcare is accelerating rapidly, with potential applications being demonstrated across various domains of medic"
tags:
  - "clippings"
---
## Abstract

### Background

Artificial intelligence (AI) research in healthcare is accelerating rapidly, with potential applications being demonstrated across various domains of medicine. However, there are currently limited examples of such techniques being successfully deployed into clinical practice. This article explores the main challenges and limitations of AI in healthcare, and considers the steps required to translate these potentially transformative technologies from research to clinical practice.

### Main body

Key challenges for the translation of AI systems in healthcare include those intrinsic to the science of machine learning, logistical difficulties in implementation, and consideration of the barriers to adoption as well as of the necessary sociocultural or pathway changes. Robust peer-reviewed clinical evaluation as part of randomised controlled trials should be viewed as the gold standard for evidence generation, but conducting these in practice may not always be appropriate or feasible. Performance metrics should aim to capture real clinical applicability and be understandable to intended users. Regulation that balances the pace of innovation with the potential for harm, alongside thoughtful post-market surveillance, is required to ensure that patients are not exposed to dangerous interventions nor deprived of access to beneficial innovations. Mechanisms to enable direct comparisons of AI systems must be developed, including the use of independent, local and representative test sets. Developers of AI algorithms must be vigilant to potential dangers, including dataset shift, accidental fitting of confounders, unintended discriminatory bias, the challenges of generalisation to new populations, and the unintended negative consequences of new algorithms on health outcomes.

### Conclusion

The safe and timely translation of AI research into clinically validated and appropriately regulated systems that can benefit everyone is challenging. Robust clinical evaluation, using metrics that are intuitive to clinicians and ideally go beyond measures of technical accuracy to include quality of care and patient outcomes, is essential. Further work is required (1) to identify themes of algorithmic bias and unfairness while developing mitigations to address these, (2) to reduce brittleness and improve generalisability, and (3) to develop methods for improved interpretability of machine learning predictions. If these goals can be achieved, the benefits for patients are likely to be transformational.

[View this article's peer review reports](https://link.springer.com/article/10.1186/s12916-019-1426-2/peer-review)

## Background

The exciting promise of artificial intelligence (AI) in healthcare has been widely reported, with potential applications across many different domains of medicine \[[^1], [^2]\]. This promise has been welcomed as healthcare systems globally struggle to deliver the ‘quadruple aim’, namely improving experience of care, improving the health of populations, reducing per capita costs of healthcare \[[^3]\], and improving the work life of healthcare providers \[[^4]\].

Nevertheless, the potential of AI in healthcare has not been realised to date, with limited existing reports of the clinical and cost benefits that have arisen from real-world use of AI algorithms in clinical practice. This article explores the main challenges and limitations of AI in healthcare, and considers the steps required to translate these potentially transformative technologies from research to clinical practice.

### The potential of artificial intelligence in healthcare

A rapidly accelerating number of academic research studies have demonstrated the various applications of AI in healthcare, including algorithms for interpreting chest radiographs \[[^5],[^6],[^7],[^8],[^9]\], detecting cancer in mammograms \[[^10], [^11]\], analysing computer tomography scans \[[^12],[^13],[^14],[^15]\], identifying brain tumours on magnetic resonance images \[[^16]\], and predicting development of Alzheimer’s disease from positron emission tomography \[[^17]\]. Applications have also been shown in pathology \[[^18]\], identifying cancerous skin lesions \[[^19],[^20],[^21],[^22]\], interpreting retinal imaging \[[^23], [^24]\], detecting arrhythmias \[[^25], [^26]\], and even identifying hyperkalaemia from electrocardiograms \[[^27]\]. Furthermore, AI has aided in polyp detection from colonoscopy \[[^28]\], improving genomics interpretation \[[^29]\], identifying genetic conditions from facial appearance \[[^30]\], and assessing embryo quality to maximise the success of in vitro fertilisation \[[^31]\].

Analysis of the immense volume of data collected from electronic health records (EHRs) offers promise in extracting clinically relevant information and making diagnostic evaluations \[[^32]\] as well as in providing real-time risk scores for transfer to intensive care \[[^33]\], predicting in-hospital mortality, readmission risk, prolonged length of stay and discharge diagnoses \[[^34]\], predicting future deterioration, including acute kidney injury \[[^35]\], improving decision-making strategies, including weaning of mechanical ventilation \[[^36]\] and management of sepsis \[[^37]\], and learning treatment policies from observational data \[[^38]\]. Proof-of-concept studies have aimed to improve the clinical workflow, including automatic extraction of semantic information from transcripts \[[^39]\], recognising speech in doctor–patient conversations \[[^40]\], predicting risk of failure to attend hospital appointments \[[^41]\], and even summarising doctor–patient consultations \[[^42]\].

Given this impressive array of studies, it is perhaps surprising that real world deployments of machine learning algorithms in clinical practice are rare. Despite this, we believe that AI will have a positive impact on many aspects of medicine. AI systems have the potential to reduce unwarranted variation in clinical practice, improve efficiency and prevent avoidable medical errors that will affect almost every patient during their lifetime \[[^43]\]. By providing novel tools to support patients and augment healthcare staff, AI could enable better care delivered closer to the patient in the community. AI tools could assist patients in playing a greater role in managing their own health, primary care physicians by allowing them to confidently manage a greater range of complex disease, and specialists by offering superhuman diagnostic performance and disease management. Finally, through the detection of novel signals of disease that clinicians are unable to perceive, AI can extract novel insights from existing data. Examples include the identification of novel predictive features for breast cancer prognosis using stromal cells (rather than the cancer cells themselves) \[[^44]\], predicting cardiovascular risk factors and sex from a fundus photograph \[[^45]\], inferring blood flow in coronary arteries from cardiac computed tomography \[[^46]\], detecting individuals with atrial fibrillation from ECG acquired during normal sinus rhythm \[[^26]\], and using retinal imaging to assist an earlier diagnosis of dementia \[[^47]\].

## The challenge of translation to clinical practice

### Retrospective versus prospective studies

While existing studies have encompassed very large numbers of patients with extensive benchmarking against expert performance, the vast majority of studies have been retrospective, meaning that they use historically labelled data to train and test algorithms. Only through prospective studies will we begin to understand the true utility of AI systems, as performance is likely to be worse when encountering real-world data that differ from that encountered in algorithm training. The limited number of prospective studies to date include diabetic retinopathy grading \[[^48],[^49],[^50]\], detection of breast cancer metastases in sentinel lymph node biopsies \[[^51], [^52]\], wrist fracture detection \[[^53]\], colonic polyp detection \[[^28], [^54]\], and detection of congenital cataracts \[[^55]\]. Consumer technology is enabling enormous prospective studies, in relation to historical standards, through the use of wearables; for example, there is an ongoing study to detect atrial fibrillation in 419,093 consenting Apple watch owners \[[^56]\].

### Peer-reviewed randomised controlled trials as an evidence gold standard

As is common in the machine learning community, many studies have been published on preprint servers only and are not submitted to peer-reviewed journals. Peer-reviewed evidence will be important for the trust and adoption of AI within the wider medical community. There are very few randomised controlled trials (RCTs) of AI systems to date; these include an algorithm to detect childhood cataracts with promising performance in a small prospective study \[[^55]\] but less accurate performance compared to senior clinicians in a diagnostic RCT \[[^57]\]; a single-blind RCT that showed a significantly reduced blind-spot rate in esophagogastroduodenoscopy \[[^58]\]; an open, non-blinded randomised trial of an automatic polyp detection algorithm for diagnostic colonoscopy demonstrating a significant increase in detection of diminutive adenomas and hyperplastic polyps \[[^59]\]; a simulated prospective, double-blind RCT of an algorithm to detect acute neurologic events \[[^60]\]; and an unmasked RCT of a system to provide automated interpretation of cardiotocographs in labour that found no improvement in clinical outcomes for mothers or babies \[[^61]\]. The final study is a cautionary example of how higher accuracy enabled by AI systems does not necessarily result in better patient outcomes \[[^61]\]. Future studies should aim to use clinical outcomes as trial endpoints to demonstrate longer-term benefit, while recognising that algorithms are likely to result in changes of the sociocultural context or care pathways; this may necessitate more sophisticated approaches to evaluation \[[^62]\].

High quality reporting of machine learning studies is critical. Only with full and clear reporting of information on all aspects of a diagnosis or prognosis model can risk of bias and potential usefulness of prediction models be adequately assessed. Machine learning studies should aim to follow best practice recommendations, such as the Transparent Reporting of a multivariable prediction model for Individual Prognosis Or Diagnosis (TRIPOD), designed to assist the reporting of studies that develop, validate or update a prediction model for either diagnostic or prognostic purposes \[[^63]\]. In addition, a new version of the TRIPOD statement that is specific to machine learning prediction algorithms (TRIPOD-ML) is in development and will focus on the introduction of machine learning prediction algorithms, establishing methodological and reporting standards for machine learning studies in healthcare \[[^64]\].

### Metrics often do not reflect clinical applicability

The term ‘AI chasm’ has been coined to reflect the fact that accuracy does not necessarily represent clinical efficacy \[[^65]\]. Despite its universal use in machine learning studies, area under the curve of a receiver operating characteristic curve is not necessarily the best metric to represent clinical applicability \[[^66]\] and is not easily understandable by many clinicians. As well as reporting sensitivity and specificity at a selected model operating point (required to turn the continuous model output into discrete decision categories), papers should include information about positive and negative predictive values. As no single measure captures all the desirable properties of a model, several measures are typically reported to summarise its performance. However, none of these measures ultimately reflect what is most important to patients, namely whether the use of the model results in a beneficial change in patient care \[[^67]\].

Clinicians need to be able to understand how the proposed algorithms could improve patient care within a relatable workflow, yet most papers do not attempt to present such information; potential approaches to this have been suggested, including decision curve analysis, which aims to quantify the net benefit of using a model to guide subsequent actions \[[^68]\]. To improve understanding, medical students and practising clinicians should be provided with an easily accessible AI curriculum to enable them to critically appraise, adopt and use AI tools safely in their practice.

### Difficulty comparing different algorithms

The comparison of algorithms across studies in an objective manner is challenging due to each study’s performance being reported using variable methodologies on different populations with different sample distributions and characteristics. To make fair comparisons, algorithms need to be subjected to comparison on the same independent test set that is representative of the target population, using the same performance metrics. Without this, clinicians will have difficulty in determining which algorithm is likely to perform best for their patients.

The curation of independent local test sets by each healthcare provider could be used to fairly compare the performance of the various available algorithms in a representative sample of their population. Such independent test sets should be constructed using an unenriched representative sample along with data that are explicitly not available to train algorithms. A supplementary local training dataset could be provided to allow fine tuning of algorithms prior to formal testing.

For researchers, comparison will become easier with the increasing availability of large, open datasets, allowing studies to benchmark their performance in a consistent manner.

### Challenges related to machine learning science

AI algorithms have the potential to suffer from a host of shortcomings, including inapplicability outside of the training domain, bias and brittleness (tendency to be easily fooled) \[[^69]\]. Important factors for consideration include dataset shift, accidentally fitting confounders rather than true signal, propagating unintentional biases in clinical practice, providing algorithms with interpretability, developing reliable measures of model confidence, and the challenge of generalisation to different populations.

### Dataset shift

Particularly important for EHR algorithms, it is easy to ignore the fact that all input data are generated within a non-stationary environment with shifting patient populations, where clinical and operational practices evolve over time \[[^70]\]. The introduction of a new predictive algorithm may cause changes in practice, resulting in a new distribution compared to that used to train the algorithm. Therefore, methods to identify drift and update models in response to deteriorating performance are critical. Mitigations to manage this effect include careful quantification of performance over time to proactively identify problems, alongside the likely requirement for periodical retraining. Data-driven testing procedures have been suggested to recommend the most appropriate updating method, from simple recalibration to full model retraining, in order to maintain performance over time \[[^71]\].

### Accidentally fitting confounders versus true signal

Machine learning algorithms will use whatever signals are available to achieve the best possible performance in the dataset used. This may include the exploitation of unknown confounders that may not be reliable, impairing the algorithm’s ability to generalise to new datasets. For instance, in one classic example, a machine learning model did not learn the intrinsic difference between dogs and wolves, but instead learned that wolves are usually pictured standing on snow, while dogs usually appear on grass \[[^72]\]. There are similar concerns in healthcare. In one study, an algorithm was more likely to classify a skin lesion as malignant if an image had a ruler in it because the presence of a ruler correlated with an increased likelihood of a cancerous lesion \[[^19]\]. The presence of surgical skin markings have also been shown to falsely increase a deep learning model’s melanoma probability scores and hence false positive rate \[[^73]\]. In another study, hip fracture detection was found to be aided by confounders, including the scanner model and scans marked ‘urgent’ \[[^74]\]. Another algorithm for detection of pneumonia on chest x-rays was able to accurately identify hospital equipment and department, learning an association between a portable x-ray machine and pneumonia \[[^75]\]. Ongoing work is required to understand the specific features being learned by neural networks and will be critical for generalisation across multiple healthcare settings.

### Challenges in generalisation to new populations and settings

The majority of AI systems are far from achieving reliable generalisability, let alone clinical applicability, for most types of medical data. A brittle model may have blind spots that can produce particularly bad decisions. Generalisation can be hard due to technical differences between sites (including differences in equipment, coding definitions, EHR systems, and laboratory equipment and assays) as well as variations in local clinical and administrative practices.

To overcome these issues, it is likely that a degree of site-specific training will be required to adapt an existing system for a new population, particularly for complex tasks like EHR predictions. Methods to detect out-of-distribution inputs and provide a reliable measure of model confidence will be important to prevent clinical decisions being made on inaccurate model outputs. For simpler tasks, including medical image classification, this problem may be less crucial and overcome by the curation of large, heterogenous, multi-centre datasets \[[^14]\]. Generalisation of model operating points may also prove challenging across new populations, as illustrated in a recent study to detect abnormal chest radiographs, where specificity at a fixed operating point varied widely, from 0.566 to 1.000, across five independent datasets \[[^5]\].

Proper assessment of real-world clinical performance and generalisation requires appropriately designed external validation involving testing of an AI system using adequately sized datasets collected from institutions other than those that provided the data for model training. This will ensure that all relevant variations in patient demographics and disease states of target patients in real-world clinical settings are adequately represented in the system where it will be applied \[[^76]\]. This practice is currently rare in the literature and is of critical concern. A recent systematic review of studies that evaluated AI algorithms for the diagnostic analysis of medical imaging found that only 6% of 516 eligible published studies performed external validation \[[^77]\].

### Algorithmic bias

Intertwined with the issue of generalisability is that of discriminatory bias. Blind spots in machine learning can reflect the worst societal biases, with a risk of unintended or unknown accuracies in minority subgroups, and there is fear over the potential for amplifying biases present in the historical data \[[^78]\]. Studies indicate that, in some current contexts, the downsides of AI systems disproportionately affect groups that are already disadvantaged by factors such as race, gender and socioeconomic background \[[^79]\]. In medicine, examples include hospital mortality prediction algorithms with varying accuracy by ethnicity \[[^80]\] and algorithms that can classify images of benign and malignant moles with accuracy similar to that of board-certified dermatologists \[[^19], [^81]\], but with underperformance on images of lesions in skin of colour due to training on open datasets of predominantly fair skinned patients. The latter is particularly concerning as patients with skin of colour already present with more advanced dermatological diseases and have lower survival rates than those with fair skin \[[^82]\].

Algorithmic unfairness can be distilled into three components, namely (1) model bias (i.e. models selected to best represent the majority and not necessarily underrepresented groups), (2) model variance (due to inadequate data from minorities), and (3) outcome noise (the effect of a set of unobserved variables that potentially interacts with model predictions, avoidable by identifying subpopulations to measure additional variables) \[[^80]\]. A greater awareness of these issues and empowering clinicians to participate critically in system design and development will help guide researchers to ensure that the correct steps are taken to quantify bias before deploying models. Algorithms should be designed with the global community in mind, and clinical validation should be performed using a representative population of the intended deployment population. Careful performance analysis by population subgroups should be performed, including age, ethnicity, sex, sociodemographic stratum and location. Analysis to understand the impact of a new algorithm is particularly important, i.e. if the spectrum of disease detected using the AI system differs from current clinical practice, then the benefits and harms of detecting this different spectrum of disease must be evaluated. In mammography, this might be the detection of less severe ductal carcinoma in situ, potentially resulting in increased treatment with little benefit in outcomes. Prospective pilots within healthcare systems should be undertaken to understand the product characteristics and identify potential pitfalls in practical deployment.

### Susceptibility to adversarial attack or manipulation

Algorithms have been shown to be susceptible to risk of adversarial attack. Although somewhat theoretical at present, an adversarial attack describes an otherwise-effective model that is susceptible to manipulation by inputs explicitly designed to fool them. For example, in one study, images of benign moles were misdiagnosed as malignant by adding adversarial noise or even just rotation \[[^83]\].

### Logistical difficulties in implementing AI systems

Many of the current challenges in translating AI algorithms to clinical practice are related to the fact that most healthcare data are not readily available for machine learning. Data are often siloed in a multitude of medical imaging archival systems, pathology systems, EHRs, electronic prescribing tools and insurance databases, which are very difficult to bring together. Adoption of unified data formats, such as Fast Healthcare Interoperability Resources \[[^84]\], offer the potential for better aggregation of data, although improved interoperability does not necessarily fix the problem of inconsistent semantic coding in EHR data \[[^85]\].

### Achieving robust regulation and rigorous quality control

A fundamental component to achieving safe and effective deployment of AI algorithms is the development of the necessary regulatory frameworks. This poses a unique challenge given the current pace of innovation, significant risks involved and the potentially fluid nature of machine learning models. Proactive regulation will give confidence to clinicians and healthcare systems. Recent U.S. Food and Drug Administration guidance has begun developing a modern regulatory framework to make sure that safe and effective artificial intelligence devices can efficiently progress to patients \[[^86]\].

It is also important to consider the regulatory impact of improvements and upgrades that providers of AI products are likely to develop throughout the life of the product. Some AI systems will be designed to improve over time, representing a challenge to traditional evaluation processes. Where AI learning is continuous, periodic system-wide updates following a full evaluation of clinical significance would be preferred, compared to continuous updates which may result in drift. The development of ongoing performance monitoring guidelines to continually calibrate models using human feedback will support the identification of performance deficits over time.

### Human barriers to AI adoption in healthcare

Even with a highly effective algorithm that overcomes all of the above challenges, human barriers to adoption are substantial. In order to ensure that this technology can reach and benefit patients, it will be important to maintain a focus on clinical applicability and patient outcomes, advance methods for algorithmic interpretability, and achieve a better understanding of human–computer interactions.

### Algorithmic interpretability is at an early stage but rapidly advancing

While AI approaches in medicine have yielded some impressive practical successes to date, their effectiveness is limited by their inability to ‘explain’ their decision-making in an understandable way \[[^87]\]. Even if we understand the underlying mathematical principles of such models, it is difficult and often impossible to interrogate the inner workings of models to understand how and why it made a certain decision. This is potentially problematic for medical applications, where there is particular demand for approaches that are not only well-performing, but also trustworthy, transparent, interpretable and explainable \[[^88]\].

Healthcare offers one of the strongest arguments in favour of explainability \[[^88], [^89]\]. Given the combination of the devastating consequences of unacceptable results, the high risk of unquantified bias that is difficult to identify a priori, and the recognised potential for models to use inappropriate confounding variables, explainability enables system verification. This improves experts’ ability to recognise system errors, detect results based upon inappropriate reasoning, and identify the work required to remove bias. In addition, AI systems are trained using large numbers of examples and may detect patterns in data that are not accessible to humans. Interpretable systems may allow humans to extract this distilled knowledge in order to acquire new scientific insights. Finally, recent European Union General Data Protection Regulation legislation mandates a ‘right to explanation’ for algorithmically generated user-level predictions that have the potential to ‘significantly affect’ users; this suggests that there must be a possibility to make results re-traceable on demand \[[^88]\].

At present, a trade-off exists between performance and explainability. The best performing models (e.g. deep learning) are often the least explainable, whereas models with poorer performance (e.g. linear regression, decision trees) are the most explainable. A key current limitation of deep learning models is that they have no explicit declarative knowledge representation, leading to considerable difficulty in generating the required explanation structures \[[^90]\]. Machine learning methods that build upon a long history of research in traditional symbolic AI techniques to allow for encoding of semantics of data and the use of ontologies to guide the learning process may permit human experts to understand and retrace decision processes more effectively \[[^91], [^92]\]. One recent approach replaced end-to-end classification with a two-stage architecture comprising segmentation and classification, allowing the clinician to interrogate the segmentation map to understand the basis of the subsequent classification \[[^24]\].

If ‘black box’ algorithms are to be used in healthcare, they need to be used with knowledge, judgement and responsibility. In the meantime, research into explainable AI and evaluation of interpretability is occurring at a rapid pace \[[^93]\]. Explainable AI approaches are likely to facilitate faster adoption of AI systems into the clinical healthcare setting, and will help foster vital transparency and trust with their users.

### Developing a better understanding of interaction between human and algorithm

We have a limited but growing understanding of how humans are affected by algorithms in clinical practice. Following the U. S. Food and Drug Administration approval of computer-aided diagnosis for mammography in the late 1990s, computer-aided diagnosis was found to significantly increase recall rate without improving outcomes \[[^94]\]. Excessive warnings and alerts are known to result in alert fatigue \[[^94], [^95]\]. It has also been shown that humans assisted by AI performed better than either alone in a study of diabetic retinopathy screening \[[^96], [^97]\]. Techniques to more meaningfully represent medical knowledge, provide explanation and facilitate improved interaction with clinicians will only improve this performance further. We need to continue gaining a better understanding of the complex and evolving relationship between clinicians and human-centred AI tools in the live clinical environment \[[^98]\].

## Conclusion

Recent advances in artificial intelligence present an exciting opportunity to improve healthcare. However, the translation of research techniques to effective clinical deployment presents a new frontier for clinical and machine learning research. Robust, prospective clinical evaluation will be essential to ensure that AI systems are safe and effective, using clinically applicable performance metrics that go beyond measures of technical accuracy to include how AI affects the quality of care, the variability of healthcare professionals, the efficiency and productivity of clinical practice and, most importantly, patient outcomes. Independent datasets that are representative of future target populations should be curated to enable the comparison of different algorithms, while carefully evaluating for signs of potential bias and fitting to unintended confounders. Developers of AI tools must be cognisant of the potential unintended consequences of their algorithms and ensure that algorithms are designed with the global community in mind. Further work to improve the interpretability of algorithms and to understand human–algorithm interactions will be essential to their future adoption and safety supported by the development of thoughtful regulatory frameworks.

## Availability of data and materials

Not applicable.

## Abbreviations

AI:

artificial intelligence

EHRs:

electronic health records

RCT:

randomised controlled trial

TRIPOD:

Transparent Reporting of a multivariable prediction model for Individual Prognosis Or Diagnosis

## References

## Acknowledgements

Not applicable.

## Funding

Google LLC.

## Ethics declarations

### Ethics approval and consent to participate

Not applicable.

### Consent for publication

Not applicable.

### Competing interests

All authors are employed by Google LLC.

## Additional information

### Publisher’s Note

Springer Nature remains neutral with regard to jurisdictional claims in published maps and institutional affiliations.

## Rights and permissions

**Open Access** This article is distributed under the terms of the Creative Commons Attribution 4.0 International License ([http://creativecommons.org/licenses/by/4.0/](http://creativecommons.org/licenses/by/4.0/)), which permits unrestricted use, distribution, and reproduction in any medium, provided you give appropriate credit to the original author(s) and the source, provide a link to the Creative Commons license, and indicate if changes were made. The Creative Commons Public Domain Dedication waiver ([http://creativecommons.org/publicdomain/zero/1.0/](http://creativecommons.org/publicdomain/zero/1.0/)) applies to the data made available in this article, unless otherwise stated.

[^1]: Topol EJ. High-performance medicine: the convergence of human and artificial intelligence. Nat Med. 2019;25:44–56.

[Article](https://doi.org/10.1038%2Fs41591-018-0300-7) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1MXmvVOgsbs%3D) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30617339) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=High-performance%20medicine%3A%20the%20convergence%20of%20human%20and%20artificial%20intelligence&journal=Nat%20Med&doi=10.1038%2Fs41591-018-0300-7&volume=25&pages=44-56&publication_year=2019&author=Topol%2CEJ)

[^2]: Esteva A, Robicquet A, Ramsundar B, Kuleshov V, DePristo M, Chou K, et al. A guide to deep learning in healthcare. Nat Med. 2019;25:24–9.

[Article](https://doi.org/10.1038%2Fs41591-018-0316-z) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1MXmvVOgsb0%3D) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30617335) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=A%20guide%20to%20deep%20learning%20in%20healthcare&journal=Nat%20Med&doi=10.1038%2Fs41591-018-0316-z&volume=25&pages=24-29&publication_year=2019&author=Esteva%2CA&author=Robicquet%2CA&author=Ramsundar%2CB&author=Kuleshov%2CV&author=DePristo%2CM&author=Chou%2CK)

[^3]: Berwick DM, Nolan TW, Whittington J. The triple aim: care, health, and cost. Health Aff. 2008;27:759–69. [https://doi.org/10.1377/hlthaff.27.3.759](https://doi.org/10.1377/hlthaff.27.3.759)

[Article](https://doi.org/10.1377%2Fhlthaff.27.3.759) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=The%20triple%20aim%3A%20care%2C%20health%2C%20and%20cost&journal=Health%20Aff&doi=10.1377%2Fhlthaff.27.3.759&volume=27&pages=759-769&publication_year=2008&author=Berwick%2CDM&author=Nolan%2CTW&author=Whittington%2CJ)

[^4]: Bodenheimer T, Sinsky C. From triple to quadruple aim: care of the patient requires care of the provider. Ann Fam Med. 2014;12:573–6.

[Article](https://doi.org/10.1370%2Fafm.1713) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=25384822) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC4226781) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=From%20triple%20to%20quadruple%20aim%3A%20care%20of%20the%20patient%20requires%20care%20of%20the%20provider&journal=Ann%20Fam%20Med&doi=10.1370%2Fafm.1713&volume=12&pages=573-576&publication_year=2014&author=Bodenheimer%2CT&author=Sinsky%2CC)

[^5]: Hwang EJ, Park S, Jin K-N, Kim JI, Choi SY, Lee JH, et al. Development and validation of a deep learning-based automated detection algorithm for major thoracic diseases on chest radiographs. JAMA Netw Open. 2019;2:e191095.

[Article](https://doi.org/10.1001%2Fjamanetworkopen.2019.1095) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30901052) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6583308) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Development%20and%20validation%20of%20a%20deep%20learning-based%20automated%20detection%20algorithm%20for%20major%20thoracic%20diseases%20on%20chest%20radiographs&journal=JAMA%20Netw%20Open&doi=10.1001%2Fjamanetworkopen.2019.1095&volume=2&publication_year=2019&author=Hwang%2CEJ&author=Park%2CS&author=Jin%2CK-N&author=Kim%2CJI&author=Choi%2CSY&author=Lee%2CJH)

[^6]: Wang X, Peng Y, Lu L, Lu Z, Bagheri M, Summers RM. ChestX-Ray8: Hospital-Scale Chest X-Ray Database and Benchmarks on Weakly-Supervised Classification and Localization of Common Thorax Diseases. 2017 IEEE Conference on Computer Vision and Pattern Recognition (CVPR); 2017. [https://doi.org/10.1109/cvpr.2017.369](https://doi.org/10.1109/cvpr.2017.369)

[Book](https://doi.org/10.1109%2Fcvpr.2017.369) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=ChestX-Ray8%3A%20Hospital-Scale%20Chest%20X-Ray%20Database%20and%20Benchmarks%20on%20Weakly-Supervised%20Classification%20and%20Localization%20of%20Common%20Thorax%20Diseases.%202017%20IEEE%20Conference%20on%20Computer%20Vision%20and%20Pattern%20Recognition%20%28CVPR%29&doi=10.1109%2Fcvpr.2017.369&publication_year=2017&author=Wang%2CX&author=Peng%2CY&author=Lu%2CL&author=Lu%2CZ&author=Bagheri%2CM&author=Summers%2CRM)

[^7]: Li Z, Wang C, Han M, Xue Y, Wei W, Li L-J, et al. Thoracic Disease Identification and Localization with Limited Supervision. 2018 IEEE/CVF Conference on Computer Vision and Pattern Recognition. p. 2018. [https://doi.org/10.1109/cvpr.2018.00865](https://doi.org/10.1109/cvpr.2018.00865)

[^8]: Singh R, Kalra MK, Nitiwarangkul C, Patti JA, Homayounieh F, Padole A, et al. Deep learning in chest radiography: detection of findings and presence of change. PLoS One. 2018;13:e0204155. [https://doi.org/10.1371/journal.pone.0204155](https://doi.org/10.1371/journal.pone.0204155)

[Article](https://doi.org/10.1371%2Fjournal.pone.0204155) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1MXjtV2mtr0%3D) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30286097) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6171827) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Deep%20learning%20in%20chest%20radiography%3A%20detection%20of%20findings%20and%20presence%20of%20change&journal=PLoS%20One&doi=10.1371%2Fjournal.pone.0204155&volume=13&publication_year=2018&author=Singh%2CR&author=Kalra%2CMK&author=Nitiwarangkul%2CC&author=Patti%2CJA&author=Homayounieh%2CF&author=Padole%2CA)

[^9]: Nam JG, Park S, Hwang EJ, Lee JH, Jin K-N, Lim KY, et al. Development and validation of deep learning–based automatic detection algorithm for malignant pulmonary nodules on chest radiographs. Radiology. 2019;290:218–28. [https://doi.org/10.1148/radiol.2018180237](https://doi.org/10.1148/radiol.2018180237)

[Article](https://doi.org/10.1148%2Fradiol.2018180237) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30251934) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Development%20and%20validation%20of%20deep%20learning%E2%80%93based%20automatic%20detection%20algorithm%20for%20malignant%20pulmonary%20nodules%20on%20chest%20radiographs&journal=Radiology.&doi=10.1148%2Fradiol.2018180237&volume=290&pages=218-228&publication_year=2019&author=Nam%2CJG&author=Park%2CS&author=Hwang%2CEJ&author=Lee%2CJH&author=Jin%2CK-N&author=Lim%2CKY)

[^10]: Geras KJ, Wolfson S, Shen Y, Wu N, Gene Kim S, Kim E, et al. High-resolution breast cancer screening with multi-view deep convolutional neural networks. arXiv. 2017; [https://arxiv.org/abs/1703.07047](https://arxiv.org/abs/1703.07047). Accessed 1 May 2019.

[^11]: Wu N, Phang J, Park J, Shen Y, Huang Z, Zorin M, et al. Deep neural networks improve radiologists’ performance in breast cancer screening. arXiv. 2019; [https://arxiv.org/abs/1903.08297](https://arxiv.org/abs/1903.08297). Accessed 1 May 2019.

[^12]: Hua K-L, Hsu C-H, Hidayati SC, Cheng W-H, Chen Y-J. Computer-aided classification of lung nodules on computed tomography images via deep learning technique. Onco Targets Ther. 2015;8:2015–22.

[CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1cXhsFegt7k%3D) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=26346558) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC4531007) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Computer-aided%20classification%20of%20lung%20nodules%20on%20computed%20tomography%20images%20via%20deep%20learning%20technique&journal=Onco%20Targets%20Ther&volume=8&pages=2015-2022&publication_year=2015&author=Hua%2CK-L&author=Hsu%2CC-H&author=Hidayati%2CSC&author=Cheng%2CW-H&author=Chen%2CY-J)

[^13]: Yasaka K, Akai H, Abe O, Kiryu S. Deep learning with convolutional neural network for differentiation of liver masses at dynamic contrast-enhanced CT: a preliminary study. Radiology. 2018;286:887–96. [https://doi.org/10.1148/radiol.2017170706](https://doi.org/10.1148/radiol.2017170706)

[Article](https://doi.org/10.1148%2Fradiol.2017170706) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=29059036) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Deep%20learning%20with%20convolutional%20neural%20network%20for%20differentiation%20of%20liver%20masses%20at%20dynamic%20contrast-enhanced%20CT%3A%20a%20preliminary%20study&journal=Radiology.&doi=10.1148%2Fradiol.2017170706&volume=286&pages=887-896&publication_year=2018&author=Yasaka%2CK&author=Akai%2CH&author=Abe%2CO&author=Kiryu%2CS)

[^14]: Chilamkurthy S, Ghosh R, Tanamala S, Biviji M, Campeau NG, Venugopal VK, et al. Deep learning algorithms for detection of critical findings in head CT scans: a retrospective study. Lancet. 2018;392:2388–96.

[Article](https://doi.org/10.1016%2FS0140-6736%2818%2931645-3) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30318264) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Deep%20learning%20algorithms%20for%20detection%20of%20critical%20findings%20in%20head%20CT%20scans%3A%20a%20retrospective%20study&journal=Lancet.&doi=10.1016%2FS0140-6736%2818%2931645-3&volume=392&pages=2388-2396&publication_year=2018&author=Chilamkurthy%2CS&author=Ghosh%2CR&author=Tanamala%2CS&author=Biviji%2CM&author=Campeau%2CNG&author=Venugopal%2CVK)

[^15]: Shadmi R, Mazo V, Bregman-Amitai O, Elnekave E. Fully-convolutional deep-learning based system for coronary calcium score prediction from non-contrast chest CT. 2018 IEEE 15th International Symposium on Biomedical Imaging (ISBI 2018); 2018. [https://doi.org/10.1109/isbi.2018.8363515](https://doi.org/10.1109/isbi.2018.8363515)

[Book](https://doi.org/10.1109%2Fisbi.2018.8363515) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Fully-convolutional%20deep-learning%20based%20system%20for%20coronary%20calcium%20score%20prediction%20from%20non-contrast%20chest%20CT.%202018%20IEEE%2015th%20International%20Symposium%20on%20Biomedical%20Imaging%20%28ISBI%202018%29&doi=10.1109%2Fisbi.2018.8363515&publication_year=2018&author=Shadmi%2CR&author=Mazo%2CV&author=Bregman-Amitai%2CO&author=Elnekave%2CE)

[^16]: Kamnitsas K, Ferrante E, Parisot S, Ledig C, Nori AV, Criminisi A, et al. DeepMedic for brain tumor segmentation. In: International Workshop on Brainlesion: Glioma, Multiple Sclerosis, Stroke and Traumatic Brain Injuries; 2016. p. 38–49. [https://doi.org/10.1007/978-3-319-55524-9\_14](https://doi.org/10.1007/978-3-319-55524-9_14)

[Chapter](https://link.springer.com/doi/10.1007/978-3-319-55524-9_14) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=DeepMedic%20for%20brain%20tumor%20segmentation&doi=10.1007%2F978-3-319-55524-9_14&pages=38-49&publication_year=2016&author=Kamnitsas%2CK&author=Ferrante%2CE&author=Parisot%2CS&author=Ledig%2CC&author=Nori%2CAV&author=Criminisi%2CA)

[^17]: Ding Y, Sohn JH, Kawczynski MG, Trivedi H, Harnish R, Jenkins NW, et al. A deep learning model to predict a diagnosis of Alzheimer disease by using F-FDG PET of the brain. Radiology. 2019;290:456–64.

[Article](https://doi.org/10.1148%2Fradiol.2018180958) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30398430) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=A%20deep%20learning%20model%20to%20predict%20a%20diagnosis%20of%20Alzheimer%20disease%20by%20using%20F-FDG%20PET%20of%20the%20brain&journal=Radiology.&doi=10.1148%2Fradiol.2018180958&volume=290&pages=456-464&publication_year=2019&author=Ding%2CY&author=Sohn%2CJH&author=Kawczynski%2CMG&author=Trivedi%2CH&author=Harnish%2CR&author=Jenkins%2CNW)

[^18]: Chang HY, Jung CK, Woo JI, Lee S, Cho J, Kim SW, et al. Artificial intelligence in pathology. J Pathol Transl Med. 2019;53:1–12.

[Article](https://doi.org/10.4132%2Fjptm.2018.12.16) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30599506) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Artificial%20intelligence%20in%20pathology&journal=J%20Pathol%20Transl%20Med&doi=10.4132%2Fjptm.2018.12.16&volume=53&pages=1-12&publication_year=2019&author=Chang%2CHY&author=Jung%2CCK&author=Woo%2CJI&author=Lee%2CS&author=Cho%2CJ&author=Kim%2CSW)

[^19]: Esteva A, Kuprel B, Novoa RA, Ko J, Swetter SM, Blau HM, et al. Dermatologist-level classification of skin cancer with deep neural networks. Nature. 2017;542:115–8.

[Article](https://doi.org/10.1038%2Fnature21056) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC2sXhsFGltrY%3D) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=28117445) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC8382232) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Dermatologist-level%20classification%20of%20skin%20cancer%20with%20deep%20neural%20networks&journal=Nature.&doi=10.1038%2Fnature21056&volume=542&pages=115-118&publication_year=2017&author=Esteva%2CA&author=Kuprel%2CB&author=Novoa%2CRA&author=Ko%2CJ&author=Swetter%2CSM&author=Blau%2CHM)

[^20]: Haenssle HA, Fink C, Schneiderbauer R, Toberer F, Buhl T, Blum A, et al. Man against machine: diagnostic performance of a deep learning convolutional neural network for dermoscopic melanoma recognition in comparison to 58 dermatologists. Ann Oncol. 2018;29:1836–42.

[Article](https://doi.org/10.1093%2Fannonc%2Fmdy166) [CAS](https://link.springer.com/articles/cas-redirect/1:STN:280:DC%2BC1MbhslCjtA%3D%3D) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=29846502) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Man%20against%20machine%3A%20diagnostic%20performance%20of%20a%20deep%20learning%20convolutional%20neural%20network%20for%20dermoscopic%20melanoma%20recognition%20in%20comparison%20to%2058%20dermatologists&journal=Ann%20Oncol&doi=10.1093%2Fannonc%2Fmdy166&volume=29&pages=1836-1842&publication_year=2018&author=Haenssle%2CHA&author=Fink%2CC&author=Schneiderbauer%2CR&author=Toberer%2CF&author=Buhl%2CT&author=Blum%2CA)

[^21]: Han SS, Kim MS, Lim W, Park GH, Park I, Chang SE. Classification of the clinical images for benign and malignant cutaneous tumors using a deep learning algorithm. J Invest Dermatol. 2018;138:1529–38.

[Article](https://doi.org/10.1016%2Fj.jid.2018.01.028) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1cXks12lsLc%3D) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=29428356) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Classification%20of%20the%20clinical%20images%20for%20benign%20and%20malignant%20cutaneous%20tumors%20using%20a%20deep%20learning%20algorithm&journal=J%20Invest%20Dermatol&doi=10.1016%2Fj.jid.2018.01.028&volume=138&pages=1529-1538&publication_year=2018&author=Han%2CSS&author=Kim%2CMS&author=Lim%2CW&author=Park%2CGH&author=Park%2CI&author=Chang%2CSE)

[^22]: Brinker TJ, Hekler A, Enk AH, Klode J, Hauschild A, Berking C, et al. Deep learning outperformed 136 of 157 dermatologists in a head-to-head dermoscopic melanoma image classification task. Eur J Cancer. 2019;113:47–54.

[Article](https://doi.org/10.1016%2Fj.ejca.2019.04.001) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30981091) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Deep%20learning%20outperformed%20136%20of%20157%20dermatologists%20in%20a%20head-to-head%20dermoscopic%20melanoma%20image%20classification%20task&journal=Eur%20J%20Cancer&doi=10.1016%2Fj.ejca.2019.04.001&volume=113&pages=47-54&publication_year=2019&author=Brinker%2CTJ&author=Hekler%2CA&author=Enk%2CAH&author=Klode%2CJ&author=Hauschild%2CA&author=Berking%2CC)

[^23]: Gulshan V, Peng L, Coram M, Stumpe MC, Wu D, Narayanaswamy A, et al. Development and validation of a deep learning algorithm for detection of diabetic retinopathy in retinal fundus photographs. JAMA. 2016;316:2402–10.

[Article](https://doi.org/10.1001%2Fjama.2016.17216) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=27898976) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Development%20and%20validation%20of%20a%20deep%20learning%20algorithm%20for%20detection%20of%20diabetic%20retinopathy%20in%20retinal%20fundus%20photographs&journal=JAMA.&doi=10.1001%2Fjama.2016.17216&volume=316&pages=2402-2410&publication_year=2016&author=Gulshan%2CV&author=Peng%2CL&author=Coram%2CM&author=Stumpe%2CMC&author=Wu%2CD&author=Narayanaswamy%2CA)

[^24]: De Fauw J, Ledsam JR, Romera-Paredes B, Nikolov S, Tomasev N, Blackwell S, et al. Clinically applicable deep learning for diagnosis and referral in retinal disease. Nat Med. 2018;24:1342–50.

[Article](https://doi.org/10.1038%2Fs41591-018-0107-6) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30104768) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1cXhsFSqtbzN) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Clinically%20applicable%20deep%20learning%20for%20diagnosis%20and%20referral%20in%20retinal%20disease&journal=Nat%20Med&doi=10.1038%2Fs41591-018-0107-6&volume=24&pages=1342-1350&publication_year=2018&author=Fauw%2CJ&author=Ledsam%2CJR&author=Romera-Paredes%2CB&author=Nikolov%2CS&author=Tomasev%2CN&author=Blackwell%2CS)

[^25]: Hannun AY, Rajpurkar P, Haghpanahi M, Tison GH, Bourn C, Turakhia MP, et al. Cardiologist-level arrhythmia detection and classification in ambulatory electrocardiograms using a deep neural network. Nat Med. 2019;25:65–9.

[Article](https://doi.org/10.1038%2Fs41591-018-0268-3) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1MXmvVOgsLs%3D) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30617320) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6784839) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Cardiologist-level%20arrhythmia%20detection%20and%20classification%20in%20ambulatory%20electrocardiograms%20using%20a%20deep%20neural%20network&journal=Nat%20Med&doi=10.1038%2Fs41591-018-0268-3&volume=25&pages=65-69&publication_year=2019&author=Hannun%2CAY&author=Rajpurkar%2CP&author=Haghpanahi%2CM&author=Tison%2CGH&author=Bourn%2CC&author=Turakhia%2CMP)

[^26]: Attia ZI, Noseworthy PA, Lopez-Jimenez F, Asirvatham SJ, Deshmukh AJ, Gersh BJ, et al. An artificial intelligence-enabled ECG algorithm for the identification of patients with atrial fibrillation during sinus rhythm: a retrospective analysis of outcome prediction. Lancet. 2019;394(10201):861–7. [https://doi.org/10.1016/S0140-6736(19)31721-0](https://doi.org/10.1016/S0140-6736\(19\)31721-0)

[Article](https://doi.org/10.1016%2FS0140-6736%2819%2931721-0) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=31378392) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=An%20artificial%20intelligence-enabled%20ECG%20algorithm%20for%20the%20identification%20of%20patients%20with%20atrial%20fibrillation%20during%20sinus%20rhythm%3A%20a%20retrospective%20analysis%20of%20outcome%20prediction&journal=Lancet.&doi=10.1016%2FS0140-6736%2819%2931721-0&volume=394&issue=10201&pages=861-867&publication_year=2019&author=Attia%2CZI&author=Noseworthy%2CPA&author=Lopez-Jimenez%2CF&author=Asirvatham%2CSJ&author=Deshmukh%2CAJ&author=Gersh%2CBJ)

[^27]: Galloway CD, Valys AV, Shreibati JB, Treiman DL, Petterson FL, Gundotra VP, et al. Development and validation of a deep-learning model to screen for hyperkalemia from the electrocardiogram. JAMA Cardiol. 2019;4(5):428–36. [https://doi.org/10.1001/jamacardio.2019.0640](https://doi.org/10.1001/jamacardio.2019.0640)

[Article](https://doi.org/10.1001%2Fjamacardio.2019.0640) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30942845) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6537816) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Development%20and%20validation%20of%20a%20deep-learning%20model%20to%20screen%20for%20hyperkalemia%20from%20the%20electrocardiogram&journal=JAMA%20Cardiol&doi=10.1001%2Fjamacardio.2019.0640&volume=4&issue=5&pages=428-436&publication_year=2019&author=Galloway%2CCD&author=Valys%2CAV&author=Shreibati%2CJB&author=Treiman%2CDL&author=Petterson%2CFL&author=Gundotra%2CVP)

[^28]: Wang P, Xiao X, Glissen Brown JR, Berzin TM, Tu M, Xiong F, et al. Development and validation of a deep-learning algorithm for the detection of polyps during colonoscopy. Nat Biomed Eng. 2018;2:741–8. [https://doi.org/10.1038/s41551-018-0301-3](https://doi.org/10.1038/s41551-018-0301-3)

[Article](https://doi.org/10.1038%2Fs41551-018-0301-3) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=31015647) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Development%20and%20validation%20of%20a%20deep-learning%20algorithm%20for%20the%20detection%20of%20polyps%20during%20colonoscopy&journal=Nat%20Biomed%20Eng&doi=10.1038%2Fs41551-018-0301-3&volume=2&pages=741-748&publication_year=2018&author=Wang%2CP&author=Xiao%2CX&author=Glissen%20Brown%2CJR&author=Berzin%2CTM&author=Tu%2CM&author=Xiong%2CF)

[^29]: Xu J, Yang P, Xue S, Sharma B, Sanchez-Martin M, Wang F, et al. Translating cancer genomics into precision medicine with artificial intelligence: applications, challenges and future perspectives. Hum Genet. 2019;138:109–24.

[Article](https://link.springer.com/doi/10.1007/s00439-019-01970-5) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1MXhtVKgtb%2FE) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30671672) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6373233) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Translating%20cancer%20genomics%20into%20precision%20medicine%20with%20artificial%20intelligence%3A%20applications%2C%20challenges%20and%20future%20perspectives&journal=Hum%20Genet&doi=10.1007%2Fs00439-019-01970-5&volume=138&pages=109-124&publication_year=2019&author=Xu%2CJ&author=Yang%2CP&author=Xue%2CS&author=Sharma%2CB&author=Sanchez-Martin%2CM&author=Wang%2CF)

[^30]: Gurovich Y, Hanani Y, Bar O, Nadav G, Fleischer N, Gelbman D, et al. Identifying facial phenotypes of genetic disorders using deep learning. Nat Med. 2019;25:60–4.

[Article](https://doi.org/10.1038%2Fs41591-018-0279-0) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1MXmvVOgsLk%3D) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30617323) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Identifying%20facial%20phenotypes%20of%20genetic%20disorders%20using%20deep%20learning&journal=Nat%20Med&doi=10.1038%2Fs41591-018-0279-0&volume=25&pages=60-64&publication_year=2019&author=Gurovich%2CY&author=Hanani%2CY&author=Bar%2CO&author=Nadav%2CG&author=Fleischer%2CN&author=Gelbman%2CD)

[^31]: Khosravi P, Kazemi E, Zhan Q, Malmsten JE, Toschi M, Zisimopoulos P, et al. Deep learning enables robust assessment and selection of human blastocysts after in vitro fertilization. NPJ Digit Med. 2019;2:21. [https://doi.org/10.1038/s41746-019-0096-y](https://doi.org/10.1038/s41746-019-0096-y)

[Article](https://doi.org/10.1038%2Fs41746-019-0096-y) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=31304368) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6550169) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Deep%20learning%20enables%20robust%20assessment%20and%20selection%20of%20human%20blastocysts%20after%20in%20vitro%20fertilization&journal=NPJ%20Digit%20Med&doi=10.1038%2Fs41746-019-0096-y&volume=2&publication_year=2019&author=Khosravi%2CP&author=Kazemi%2CE&author=Zhan%2CQ&author=Malmsten%2CJE&author=Toschi%2CM&author=Zisimopoulos%2CP)

[^32]: Liang H, Tsui BY, Ni H, Valentim CCS, Baxter SL, Liu G, et al. Evaluation and accurate diagnoses of pediatric diseases using artificial intelligence. Nat Med. 2019;25:433–8.

[Article](https://doi.org/10.1038%2Fs41591-018-0335-9) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1MXmsVymtL4%3D) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30742121) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Evaluation%20and%20accurate%20diagnoses%20of%20pediatric%20diseases%20using%20artificial%20intelligence&journal=Nat%20Med&doi=10.1038%2Fs41591-018-0335-9&volume=25&pages=433-438&publication_year=2019&author=Liang%2CH&author=Tsui%2CBY&author=Ni%2CH&author=Valentim%2CCCS&author=Baxter%2CSL&author=Liu%2CG)

[^33]: Escobar GJ, Turk BJ, Ragins A, Ha J, Hoberman B, LeVine SM, et al. Piloting electronic medical record-based early detection of inpatient deterioration in community hospitals. J Hosp Med. 2016;11(Suppl 1):S18–24.

[Article](https://doi.org/10.1002%2Fjhm.2652) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=27805795) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Piloting%20electronic%20medical%20record-based%20early%20detection%20of%20inpatient%20deterioration%20in%20community%20hospitals&journal=J%20Hosp%20Med&doi=10.1002%2Fjhm.2652&volume=11&issue=Suppl%201&pages=S18-S24&publication_year=2016&author=Escobar%2CGJ&author=Turk%2CBJ&author=Ragins%2CA&author=Ha%2CJ&author=Hoberman%2CB&author=LeVine%2CSM)

[^34]: Rajkomar A, Oren E, Chen K, Dai AM, Hajaj N, Hardt M, et al. Scalable and accurate deep learning with electronic health records. NPJ Digit Med. 2018;1:18. [https://doi.org/10.1038/s41746-018-0029-1](https://doi.org/10.1038/s41746-018-0029-1)

[Article](https://doi.org/10.1038%2Fs41746-018-0029-1) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=31304302) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6550175) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Scalable%20and%20accurate%20deep%20learning%20with%20electronic%20health%20records&journal=NPJ%20Digit%20Med&doi=10.1038%2Fs41746-018-0029-1&volume=1&publication_year=2018&author=Rajkomar%2CA&author=Oren%2CE&author=Chen%2CK&author=Dai%2CAM&author=Hajaj%2CN&author=Hardt%2CM)

[^35]: Tomašev N, Glorot X, Rae JW, Zielinski M, Askham H, Saraiva A, et al. A clinically applicable approach to continuous prediction of future acute kidney injury. Nature. 2019;572:116–9.

[Article](https://doi.org/10.1038%2Fs41586-019-1390-1) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=31367026) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1MXhsFShu7fO) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6722431) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=A%20clinically%20applicable%20approach%20to%20continuous%20prediction%20of%20future%20acute%20kidney%20injury&journal=Nature.&doi=10.1038%2Fs41586-019-1390-1&volume=572&pages=116-119&publication_year=2019&author=Toma%C5%A1ev%2CN&author=Glorot%2CX&author=Rae%2CJW&author=Zielinski%2CM&author=Askham%2CH&author=Saraiva%2CA)

[^36]: Prasad N, Cheng L-F, Chivers C, Draugelis M, Engelhardt BE. A reinforcement learning approach to weaning of mechanical ventilation in intensive care units. arXiv. 2017; [https://arxiv.org/abs/1704.06300](https://arxiv.org/abs/1704.06300). Accessed 1 May 2019.

[^37]: Raghu A, Komorowski M, Ahmed I, Celi L, Szolovits P, Ghassemi M. Deep reinforcement learning for sepsis treatment. arXiv. 2017; [https://arxiv.org/abs/1711.09602](https://arxiv.org/abs/1711.09602). Accessed 1 May 2019.

[^38]: Gottesman O, Johansson F, Meier J, Dent J, Lee D, Srinivasan S, et al. Evaluating reinforcement learning algorithms in observational health settings. arXiv. 2018; [https://arxiv.org/abs/1805.12298](https://arxiv.org/abs/1805.12298). Accessed 1 May 2019.

[^39]: Kannan A, Chen K, Jaunzeikare D, Rajkomar A. Semi-supervised learning for information extraction from dialogue. Interspeech. 2018;2018:2077–81. [https://doi.org/10.21437/interspeech.2018-1318](https://doi.org/10.21437/interspeech.2018-1318)

[Article](https://doi.org/10.21437%2Finterspeech.2018-1318) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Semi-supervised%20learning%20for%20information%20extraction%20from%20dialogue&journal=Interspeech&doi=10.21437%2Finterspeech.2018-1318&volume=2018&pages=2077-2081&publication_year=2018&author=Kannan%2CA&author=Chen%2CK&author=Jaunzeikare%2CD&author=Rajkomar%2CA)

[^40]: Chiu C-C, Tripathi A, Chou K, Co C, Jaitly N, Jaunzeikare D, et al. Speech recognition for medical conversations. arXiv. 2017; [https://arxiv.org/abs/1711.07274](https://arxiv.org/abs/1711.07274). Accessed 1 May 2019.

[^41]: Nelson A, Herron D, Rees G, Nachev P. Predicting scheduled hospital attendance with artificial intelligence. NPJ Digit Med. 2019;2:26. [https://doi.org/10.1038/s41746-019-0103-3](https://doi.org/10.1038/s41746-019-0103-3)

[Article](https://doi.org/10.1038%2Fs41746-019-0103-3) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=31304373) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6550247) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Predicting%20scheduled%20hospital%20attendance%20with%20artificial%20intelligence&journal=NPJ%20Digit%20Med&doi=10.1038%2Fs41746-019-0103-3&volume=2&publication_year=2019&author=Nelson%2CA&author=Herron%2CD&author=Rees%2CG&author=Nachev%2CP)

[^42]: Rajkomar A, Kannan A, Chen K, Vardoulakis L, Chou K, Cui C, et al. Automatically charting symptoms from patient-physician conversations using machine learning. JAMA Intern Med. 2019;179(6):836–8. [https://doi.org/10.1001/jamainternmed.2018.8558](https://doi.org/10.1001/jamainternmed.2018.8558)

[Article](https://doi.org/10.1001%2Fjamainternmed.2018.8558) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30907920) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6547250) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Automatically%20charting%20symptoms%20from%20patient-physician%20conversations%20using%20machine%20learning&journal=JAMA%20Intern%20Med&doi=10.1001%2Fjamainternmed.2018.8558&volume=179&issue=6&pages=836-838&publication_year=2019&author=Rajkomar%2CA&author=Kannan%2CA&author=Chen%2CK&author=Vardoulakis%2CL&author=Chou%2CK&author=Cui%2CC)

[^43]: McGlynn EA, McDonald KM, Cassel CK. Measurement is essential for improving diagnosis and reducing diagnostic error: a report from the institute of medicine. JAMA. 2015;314:2501–2.

[Article](https://doi.org/10.1001%2Fjama.2015.13453) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC28XnsFCitbc%3D) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=26571126) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Measurement%20is%20essential%20for%20improving%20diagnosis%20and%20reducing%20diagnostic%20error%3A%20a%20report%20from%20the%20institute%20of%20medicine&journal=JAMA.&doi=10.1001%2Fjama.2015.13453&volume=314&pages=2501-2502&publication_year=2015&author=McGlynn%2CEA&author=McDonald%2CKM&author=Cassel%2CCK)

[^44]: Beck AH, Sangoi AR, Leung S, Marinelli RJ, Nielsen TO, van de Vijver MJ, et al. Systematic analysis of breast cancer morphology uncovers stromal features associated with survival. Sci Transl Med. 2011;3:108ra113.

[Article](https://doi.org/10.1126%2Fscitranslmed.3002564) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=22072638) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Systematic%20analysis%20of%20breast%20cancer%20morphology%20uncovers%20stromal%20features%20associated%20with%20survival&journal=Sci%20Transl%20Med&doi=10.1126%2Fscitranslmed.3002564&volume=3&publication_year=2011&author=Beck%2CAH&author=Sangoi%2CAR&author=Leung%2CS&author=Marinelli%2CRJ&author=Vijver%2CMJ)

[^45]: Poplin R, Varadarajan AV, Blumer K, Liu Y, McConnell MV, Corrado GS, et al. Prediction of cardiovascular risk factors from retinal fundus photographs via deep learning. Nat Biomed Eng. 2018;2:158–64.

[Article](https://doi.org/10.1038%2Fs41551-018-0195-0) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=31015713) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Prediction%20of%20cardiovascular%20risk%20factors%20from%20retinal%20fundus%20photographs%20via%20deep%20learning&journal=Nat%20Biomed%20Eng&doi=10.1038%2Fs41551-018-0195-0&volume=2&pages=158-164&publication_year=2018&author=Poplin%2CR&author=Varadarajan%2CAV&author=Blumer%2CK&author=Liu%2CY&author=McConnell%2CMV&author=Corrado%2CGS)

[^46]: Zarins CK, Taylor CA, Min JK. Computed fractional flow reserve (FFTCT) derived from coronary CT angiography. J Cardiovasc Transl Res. 2013;6:708–14. [https://doi.org/10.1007/s12265-013-9498-4](https://doi.org/10.1007/s12265-013-9498-4)

[Article](https://link.springer.com/doi/10.1007/s12265-013-9498-4) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=23934536) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3790916) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Computed%20fractional%20flow%20reserve%20%28FFTCT%29%20derived%20from%20coronary%20CT%20angiography&journal=J%20Cardiovasc%20Transl%20Res&doi=10.1007%2Fs12265-013-9498-4&volume=6&pages=708-714&publication_year=2013&author=Zarins%2CCK&author=Taylor%2CCA&author=Min%2CJK)

[^47]: Mutlu U, Colijn JM, Ikram MA, Bonnemaijer PWM, Licher S, Wolters FJ, et al. Association of retinal neurodegeneration on optical coherence tomography with dementia: a population-based study. JAMA Neurol. 2018;75:1256–63.

[Article](https://doi.org/10.1001%2Fjamaneurol.2018.1563) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=29946702) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6233847) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Association%20of%20retinal%20neurodegeneration%20on%20optical%20coherence%20tomography%20with%20dementia%3A%20a%20population-based%20study&journal=JAMA%20Neurol&doi=10.1001%2Fjamaneurol.2018.1563&volume=75&pages=1256-1263&publication_year=2018&author=Mutlu%2CU&author=Colijn%2CJM&author=Ikram%2CMA&author=Bonnemaijer%2CPWM&author=Licher%2CS&author=Wolters%2CFJ)

[^48]: Abràmoff MD, Lavin PT, Birch M, Shah N, Folk JC. Pivotal trial of an autonomous AI-based diagnostic system for detection of diabetic retinopathy in primary care offices. NPJ Digit Med. 2018;1:39. [https://doi.org/10.1038/s41746-018-0040-6](https://doi.org/10.1038/s41746-018-0040-6)

[Article](https://doi.org/10.1038%2Fs41746-018-0040-6) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=31304320) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6550188) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Pivotal%20trial%20of%20an%20autonomous%20AI-based%20diagnostic%20system%20for%20detection%20of%20diabetic%20retinopathy%20in%20primary%20care%20offices&journal=NPJ%20Digit%20Med&doi=10.1038%2Fs41746-018-0040-6&volume=1&publication_year=2018&author=Abr%C3%A0moff%2CMD&author=Lavin%2CPT&author=Birch%2CM&author=Shah%2CN&author=Folk%2CJC)

[^49]: Kanagasingam Y, Xiao D, Vignarajan J, Preetham A, Tay-Kearney M-L, Mehrotra A. Evaluation of artificial intelligence-based grading of diabetic retinopathy in primary care. JAMA Netw Open. 2018;1:e182665. [https://doi.org/10.1001/jamanetworkopen.2018.2665](https://doi.org/10.1001/jamanetworkopen.2018.2665)

[Article](https://doi.org/10.1001%2Fjamanetworkopen.2018.2665) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30646178) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6324474) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Evaluation%20of%20artificial%20intelligence-based%20grading%20of%20diabetic%20retinopathy%20in%20primary%20care&journal=JAMA%20Netw%20Open&doi=10.1001%2Fjamanetworkopen.2018.2665&volume=1&publication_year=2018&author=Kanagasingam%2CY&author=Xiao%2CD&author=Vignarajan%2CJ&author=Preetham%2CA&author=Tay-Kearney%2CM-L&author=Mehrotra%2CA)

[^50]: Bellemo V, Lim ZW, Lim G, Nguyen QD, Xie Y, Yip MYT, et al. Artificial intelligence using deep learning to screen for referable and vision-threatening diabetic retinopathy in Africa: a clinical validation study. Lancet Digit Health. 2019;1:e35–44.

[Article](https://doi.org/10.1016%2FS2589-7500%2819%2930004-4) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=33323239) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Artificial%20intelligence%20using%20deep%20learning%20to%20screen%20for%20referable%20and%20vision-threatening%20diabetic%20retinopathy%20in%20Africa%3A%20a%20clinical%20validation%20study&journal=Lancet%20Digit%20Health&doi=10.1016%2FS2589-7500%2819%2930004-4&volume=1&pages=e35-e44&publication_year=2019&author=Bellemo%2CV&author=Lim%2CZW&author=Lim%2CG&author=Nguyen%2CQD&author=Xie%2CY&author=Yip%2CMYT)

[^51]: Liu Y, Kohlberger T, Norouzi M, Dahl GE, Smith JL, Mohtashamian A, et al. Artificial intelligence-based breast cancer nodal metastasis detection: insights into the black box for pathologists. Arch Pathol Lab Med. 2018;143(7):859–68. [https://doi.org/10.5858/arpa.2018-0147-oa](https://doi.org/10.5858/arpa.2018-0147-oa)

[Article](https://doi.org/10.5858%2Farpa.2018-0147-oa) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30295070) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Artificial%20intelligence-based%20breast%20cancer%20nodal%20metastasis%20detection%3A%20insights%20into%20the%20black%20box%20for%20pathologists&journal=Arch%20Pathol%20Lab%20Med&doi=10.5858%2Farpa.2018-0147-oa&volume=143&issue=7&pages=859-868&publication_year=2018&author=Liu%2CY&author=Kohlberger%2CT&author=Norouzi%2CM&author=Dahl%2CGE&author=Smith%2CJL&author=Mohtashamian%2CA)

[^52]: Steiner DF, MacDonald R, Liu Y, Truszkowski P, Hipp JD, Gammage C, et al. Impact of deep learning assistance on the histopathologic review of lymph nodes for metastatic breast cancer. Am J Surg Pathol. 2018;42:1636–46.

[Article](https://doi.org/10.1097%2FPAS.0000000000001151) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30312179) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6257102) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Impact%20of%20deep%20learning%20assistance%20on%20the%20histopathologic%20review%20of%20lymph%20nodes%20for%20metastatic%20breast%20cancer&journal=Am%20J%20Surg%20Pathol&doi=10.1097%2FPAS.0000000000001151&volume=42&pages=1636-1646&publication_year=2018&author=Steiner%2CDF&author=MacDonald%2CR&author=Liu%2CY&author=Truszkowski%2CP&author=Hipp%2CJD&author=Gammage%2CC)

[^53]: Lindsey R, Daluiski A, Chopra S, Lachapelle A, Mozer M, Sicular S, et al. Deep neural network improves fracture detection by clinicians. Proc Natl Acad Sci U S A. 2018;115:11591–6.

[Article](https://doi.org/10.1073%2Fpnas.1806905115) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1cXitFSjsr3E) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30348771) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6233134) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Deep%20neural%20network%20improves%20fracture%20detection%20by%20clinicians&journal=Proc%20Natl%20Acad%20Sci%20U%20S%20A&doi=10.1073%2Fpnas.1806905115&volume=115&pages=11591-11596&publication_year=2018&author=Lindsey%2CR&author=Daluiski%2CA&author=Chopra%2CS&author=Lachapelle%2CA&author=Mozer%2CM&author=Sicular%2CS)

[^54]: Mori Y, Kudo S-E, Misawa M, Saito Y, Ikematsu H, Hotta K, et al. Real-time use of artificial intelligence in identification of diminutive polyps during colonoscopy. Ann Intern Med. 2018;169:357. [https://doi.org/10.7326/m18-0249](https://doi.org/10.7326/m18-0249)

[Article](https://doi.org/10.7326%2Fm18-0249) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30105375) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Real-time%20use%20of%20artificial%20intelligence%20in%20identification%20of%20diminutive%20polyps%20during%20colonoscopy&journal=Ann%20Intern%20Med&doi=10.7326%2Fm18-0249&volume=169&publication_year=2018&author=Mori%2CY&author=Kudo%2CS-E&author=Misawa%2CM&author=Saito%2CY&author=Ikematsu%2CH&author=Hotta%2CK)

[^55]: Long E, Lin H, Liu Z, Wu X, Wang L, Jiang J, et al. An artificial intelligence platform for the multihospital collaborative management of congenital cataracts. Nat Biomed Eng. 2017;1:0024. [https://doi.org/10.1038/s41551-016-0024](https://doi.org/10.1038/s41551-016-0024)

[Article](https://doi.org/10.1038%2Fs41551-016-0024) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=An%20artificial%20intelligence%20platform%20for%20the%20multihospital%20collaborative%20management%20of%20congenital%20cataracts&journal=Nat%20Biomed%20Eng&doi=10.1038%2Fs41551-016-0024&volume=1&publication_year=2017&author=Long%2CE&author=Lin%2CH&author=Liu%2CZ&author=Wu%2CX&author=Wang%2CL&author=Jiang%2CJ)

[^56]: Turakhia MP, Desai M, Hedlin H, Rajmane A, Talati N, Ferris T, et al. Rationale and design of a large-scale, app-based study to identify cardiac arrhythmias using a smartwatch: The Apple Heart Study. Am Heart J. 2019;207:66–75.

[Article](https://doi.org/10.1016%2Fj.ahj.2018.09.002) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30392584) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Rationale%20and%20design%20of%20a%20large-scale%2C%20app-based%20study%20to%20identify%20cardiac%20arrhythmias%20using%20a%20smartwatch%3A%20The%20Apple%20Heart%20Study&journal=Am%20Heart%20J&doi=10.1016%2Fj.ahj.2018.09.002&volume=207&pages=66-75&publication_year=2019&author=Turakhia%2CMP&author=Desai%2CM&author=Hedlin%2CH&author=Rajmane%2CA&author=Talati%2CN&author=Ferris%2CT)

[^57]: Lin H, Li R, Liu Z, Chen J, Yang Y, Chen H, et al. Diagnostic efficacy and therapeutic decision-making capacity of an artificial intelligence platform for childhood cataracts in eye clinics: a multicentre randomized controlled trial. EClinicalMedicine. 2019;9:52–9. [https://doi.org/10.1016/j.eclinm.2019.03.001](https://doi.org/10.1016/j.eclinm.2019.03.001)

[Article](https://doi.org/10.1016%2Fj.eclinm.2019.03.001) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=31143882) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6510889) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Diagnostic%20efficacy%20and%20therapeutic%20decision-making%20capacity%20of%20an%20artificial%20intelligence%20platform%20for%20childhood%20cataracts%20in%20eye%20clinics%3A%20a%20multicentre%20randomized%20controlled%20trial&journal=EClinicalMedicine.&doi=10.1016%2Fj.eclinm.2019.03.001&volume=9&pages=52-59&publication_year=2019&author=Lin%2CH&author=Li%2CR&author=Liu%2CZ&author=Chen%2CJ&author=Yang%2CY&author=Chen%2CH)

[^58]: Wu L, Zhang J, Zhou W, An P, Shen L, Liu J, et al. Randomised controlled trial of WISENSE, a real-time quality improving system for monitoring blind spots during esophagogastroduodenoscopy. Gut. 2019. [https://doi.org/10.1136/gutjnl-2018-317366](https://doi.org/10.1136/gutjnl-2018-317366)

[^59]: Wang P, Berzin TM, Brown JRG, Bharadwaj S, Becq A, Xiao X, et al. Real-time automatic detection system increases colonoscopic polyp and adenoma detection rates: a prospective randomised controlled study. Gut. 2019;68(10):1813–9. [https://doi.org/10.1136/gutjnl-2018-317500](https://doi.org/10.1136/gutjnl-2018-317500)

[Article](https://doi.org/10.1136%2Fgutjnl-2018-317500) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30814121) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Real-time%20automatic%20detection%20system%20increases%20colonoscopic%20polyp%20and%20adenoma%20detection%20rates%3A%20a%20prospective%20randomised%20controlled%20study&journal=Gut.&doi=10.1136%2Fgutjnl-2018-317500&volume=68&issue=10&pages=1813-1819&publication_year=2019&author=Wang%2CP&author=Berzin%2CTM&author=Brown%2CJRG&author=Bharadwaj%2CS&author=Becq%2CA&author=Xiao%2CX)

[^60]: Titano JJ, Badgeley M, Schefflein J, Pain M, Su A, Cai M, et al. Automated deep-neural-network surveillance of cranial images for acute neurologic events. Nat Med. 2018;24:1337–41.

[Article](https://doi.org/10.1038%2Fs41591-018-0147-y) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1cXhsFSqtbzM) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30104767) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Automated%20deep-neural-network%20surveillance%20of%20cranial%20images%20for%20acute%20neurologic%20events&journal=Nat%20Med&doi=10.1038%2Fs41591-018-0147-y&volume=24&pages=1337-1341&publication_year=2018&author=Titano%2CJJ&author=Badgeley%2CM&author=Schefflein%2CJ&author=Pain%2CM&author=Su%2CA&author=Cai%2CM)

[^61]: Brocklehurst P, Field D, Greene K, Juszczak E, Keith R, Kenyon S, et al. Computerised interpretation of fetal heart rate during labour (INFANT): a randomised controlled trial. Lancet. 2017;389:1719–29. [https://doi.org/10.1016/s0140-6736(17)30568-8](https://doi.org/10.1016/s0140-6736\(17\)30568-8)

[Article](https://doi.org/10.1016%2Fs0140-6736%2817%2930568-8) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Computerised%20interpretation%20of%20fetal%20heart%20rate%20during%20labour%20%28INFANT%29%3A%20a%20randomised%20controlled%20trial&journal=Lancet.&doi=10.1016%2Fs0140-6736%2817%2930568-8&volume=389&pages=1719-1729&publication_year=2017&author=Brocklehurst%2CP&author=Field%2CD&author=Greene%2CK&author=Juszczak%2CE&author=Keith%2CR&author=Kenyon%2CS)

[^62]: Craig P, Dieppe P, Macintyre S, Michie S, Nazareth I, Petticrew M. Developing and evaluating complex interventions: an introduction to the new Medical Research Council guidance. In: Evidence-based Public Health: Effectiveness and Efficiency; 2009. p. 185–202. [https://doi.org/10.1093/acprof:oso/9780199563623.003.012](https://doi.org/10.1093/acprof:oso/9780199563623.003.012)

[Chapter](https://doi.org/10.1093%2Facprof%3Aoso%2F9780199563623.003.012) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Developing%20and%20evaluating%20complex%20interventions%3A%20an%20introduction%20to%20the%20new%20Medical%20Research%20Council%20guidance&doi=10.1093%2Facprof%3Aoso%2F9780199563623.003.012&pages=185-202&publication_year=2009&author=Craig%2CP&author=Dieppe%2CP&author=Macintyre%2CS&author=Michie%2CS&author=Nazareth%2CI&author=Petticrew%2CM)

[^63]: Collins GS, Reitsma JB, Altman DG, Moons KGM. Transparent Reporting of a Multivariable Prediction Model for Individual Prognosis or Diagnosis (TRIPOD). Circulation. 2015;131:211–9. [https://doi.org/10.1161/circulationaha.114.014508](https://doi.org/10.1161/circulationaha.114.014508)

[Article](https://doi.org/10.1161%2Fcirculationaha.114.014508) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=25561516) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC4297220) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Transparent%20Reporting%20of%20a%20Multivariable%20Prediction%20Model%20for%20Individual%20Prognosis%20or%20Diagnosis%20%28TRIPOD%29&journal=Circulation.&doi=10.1161%2Fcirculationaha.114.014508&volume=131&pages=211-219&publication_year=2015&author=Collins%2CGS&author=Reitsma%2CJB&author=Altman%2CDG&author=Moons%2CKGM)

[^64]: Collins GS, Moons KGM. Reporting of artificial intelligence prediction models. Lancet. 2019;393:1577–9.

[Article](https://doi.org/10.1016%2FS0140-6736%2819%2930037-6) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=31007185) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Reporting%20of%20artificial%20intelligence%20prediction%20models&journal=Lancet.&doi=10.1016%2FS0140-6736%2819%2930037-6&volume=393&pages=1577-1579&publication_year=2019&author=Collins%2CGS&author=Moons%2CKGM)

[^65]: Keane PA, Topol EJ. With an eye to AI and autonomous diagnosis. NPJ Digit Med. 2018;1:40. [https://doi.org/10.1038/s41746-018-0048-y](https://doi.org/10.1038/s41746-018-0048-y)

[Article](https://doi.org/10.1038%2Fs41746-018-0048-y) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=31304321) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6550235) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=With%20an%20eye%20to%20AI%20and%20autonomous%20diagnosis&journal=NPJ%20Digit%20Med&doi=10.1038%2Fs41746-018-0048-y&volume=1&publication_year=2018&author=Keane%2CPA&author=Topol%2CEJ)

[^66]: Saito T, Rehmsmeier M. The precision-recall plot is more informative than the ROC plot when evaluating binary classifiers on imbalanced datasets. PLoS One. 2015;10:e0118432. [https://doi.org/10.1371/journal.pone.0118432](https://doi.org/10.1371/journal.pone.0118432)

[Article](https://doi.org/10.1371%2Fjournal.pone.0118432) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC2MXhslSjurbF) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=25738806) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC4349800) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=The%20precision-recall%20plot%20is%20more%20informative%20than%20the%20ROC%20plot%20when%20evaluating%20binary%20classifiers%20on%20imbalanced%20datasets&journal=PLoS%20One&doi=10.1371%2Fjournal.pone.0118432&volume=10&publication_year=2015&author=Saito%2CT&author=Rehmsmeier%2CM)

[^67]: Shah NH, Milstein A, Bagley PhD SC. Making machine learning models clinically useful. JAMA. 2019. [https://doi.org/10.1001/jama.2019.10306](https://doi.org/10.1001/jama.2019.10306)

[^68]: Vickers AJ, Cronin AM, Elkin EB, Gonen M. Extensions to decision curve analysis, a novel method for evaluating diagnostic tests, prediction models and molecular markers. BMC Med Inform Decis Mak. 2008;8:53.

[Article](https://link.springer.com/doi/10.1186/1472-6947-8-53) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=19036144) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC2611975) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Extensions%20to%20decision%20curve%20analysis%2C%20a%20novel%20method%20for%20evaluating%20diagnostic%20tests%2C%20prediction%20models%20and%20molecular%20markers&journal=BMC%20Med%20Inform%20Decis%20Mak&doi=10.1186%2F1472-6947-8-53&volume=8&publication_year=2008&author=Vickers%2CAJ&author=Cronin%2CAM&author=Elkin%2CEB&author=Gonen%2CM)

[^69]: Marcus G. Deep learning: a critical appraisal. arXiv. 2018; [https://arxiv.org/abs/1801.00631](https://arxiv.org/abs/1801.00631). Accessed 1 May 2019.

[^70]: Nestor B, McDermott MBA, Chauhan G, Naumann T, Hughes MC, Goldenberg A, et al. Rethinking clinical prediction: why machine learning must consider year of care and feature aggregation. In: Machine Learning for Health (ML4H): NeurIPS; 2018. [https://arxiv.org/abs/1811.12583](https://arxiv.org/abs/1811.12583). Accessed 1 May 2019.

[^71]: Davis SE, Greevy RA, Fonnesbeck C, Lasko TA, Walsh CG, Matheny ME. A nonparametric updating method to correct clinical prediction model drift. J Am Med Inform Assoc. 2019. [https://doi.org/10.1093/jamia/ocz127](https://doi.org/10.1093/jamia/ocz127)

[^72]: Ribeiro M, Singh S, Guestrin C. “Why Should I Trust You?”: Explaining the Predictions of Any Classifier. Proceedings of the 2016 Conference of the North American Chapter of the Association for Computational Linguistics: Demonstrations; 2016. [https://doi.org/10.18653/v1/n16-3020](https://doi.org/10.18653/v1/n16-3020)

[Book](https://doi.org/10.18653%2Fv1%2Fn16-3020) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=%E2%80%9CWhy%20Should%20I%20Trust%20You%3F%E2%80%9D%3A%20Explaining%20the%20Predictions%20of%20Any%20Classifier.%20Proceedings%20of%20the%202016%20Conference%20of%20the%20North%20American%20Chapter%20of%20the%20Association%20for%20Computational%20Linguistics%3A%20Demonstrations&doi=10.18653%2Fv1%2Fn16-3020&publication_year=2016&author=Ribeiro%2CM&author=Singh%2CS&author=Guestrin%2CC)

[^73]: Winkler JK, Fink C, Toberer F, Enk A, Deinlein T, Hofmann-Wellenhof R, et al. Association between surgical skin markings in dermoscopic images and diagnostic performance of a deep learning convolutional neural network for melanoma recognition. JAMA Dermatol. 2019. [https://doi.org/10.1001/jamadermatol.2019.1735](https://doi.org/10.1001/jamadermatol.2019.1735)

[^74]: Badgeley MA, Zech JR, Oakden-Rayner L, Glicksberg BS, Liu M, Gale W, et al. Deep learning predicts hip fracture using confounding patient and healthcare variables. arXiv. 2018; [https://arxiv.org/abs/1811.03695](https://arxiv.org/abs/1811.03695). Accessed 1 May 2019.

[^75]: Zech JR, Badgeley MA, Liu M, Costa AB, Titano JJ, Oermann EK. Variable generalization performance of a deep learning model to detect pneumonia in chest radiographs: a cross-sectional study. PLoS Med. 2018;15:e1002683.

[Article](https://doi.org/10.1371%2Fjournal.pmed.1002683) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30399157) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6219764) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Variable%20generalization%20performance%20of%20a%20deep%20learning%20model%20to%20detect%20pneumonia%20in%20chest%20radiographs%3A%20a%20cross-sectional%20study&journal=PLoS%20Med&doi=10.1371%2Fjournal.pmed.1002683&volume=15&publication_year=2018&author=Zech%2CJR&author=Badgeley%2CMA&author=Liu%2CM&author=Costa%2CAB&author=Titano%2CJJ&author=Oermann%2CEK)

[^76]: Debray TPA, Vergouwe Y, Koffijberg H, Nieboer D, Steyerberg EW, Moons KGM. A new framework to enhance the interpretation of external validation studies of clinical prediction models. J Clin Epidemiol. 2015;68:279–89.

[Article](https://doi.org/10.1016%2Fj.jclinepi.2014.06.018) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=25179855) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=A%20new%20framework%20to%20enhance%20the%20interpretation%20of%20external%20validation%20studies%20of%20clinical%20prediction%20models&journal=J%20Clin%20Epidemiol&doi=10.1016%2Fj.jclinepi.2014.06.018&volume=68&pages=279-289&publication_year=2015&author=Debray%2CTPA&author=Vergouwe%2CY&author=Koffijberg%2CH&author=Nieboer%2CD&author=Steyerberg%2CEW&author=Moons%2CKGM)

[^77]: Kim DW, Jang HY, Kim KW, Shin Y, Park SH. Design characteristics of studies reporting the performance of artificial intelligence algorithms for diagnostic analysis of medical images: results from recently published papers. Korean J Radiol. 2019;20:405–10.

[Article](https://doi.org/10.3348%2Fkjr.2019.0025) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30799571) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC6389801) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Design%20characteristics%20of%20studies%20reporting%20the%20performance%20of%20artificial%20intelligence%20algorithms%20for%20diagnostic%20analysis%20of%20medical%20images%3A%20results%20from%20recently%20published%20papers&journal=Korean%20J%20Radiol&doi=10.3348%2Fkjr.2019.0025&volume=20&pages=405-410&publication_year=2019&author=Kim%2CDW&author=Jang%2CHY&author=Kim%2CKW&author=Shin%2CY&author=Park%2CSH)

[^78]: Crawford K, Calo R. There is a blind spot in AI research. Nature. 2016;538:311–3.

[Article](https://doi.org/10.1038%2F538311a) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC28XhslWhsLvL) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=27762391) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=There%20is%20a%20blind%20spot%20in%20AI%20research&journal=Nature.&doi=10.1038%2F538311a&volume=538&pages=311-313&publication_year=2016&author=Crawford%2CK&author=Calo%2CR)

[^79]: Barocas S, Selbst AD. Big Data’s Disparate Impact. 104 California Law Review 671; 2016. [https://doi.org/10.2139/ssrn.2477899](https://doi.org/10.2139/ssrn.2477899)

[Book](https://doi.org/10.2139%2Fssrn.2477899) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Big%20Data%E2%80%99s%20Disparate%20Impact.%20104%20California%20Law%20Review%20671&doi=10.2139%2Fssrn.2477899&publication_year=2016&author=Barocas%2CS&author=Selbst%2CAD)

[^80]: Chen IY, Johansson FD, Sontag D. Why Is My Classifier Discriminatory? In: 32nd Conference on Neural Information Processing Systems (NeurIPS). 2018. [http://papers.nips.cc/paper/7613-why-is-my-classifier-discriminatory.pdf](http://papers.nips.cc/paper/7613-why-is-my-classifier-discriminatory.pdf)

[Google Scholar](http://scholar.google.com/scholar_lookup?&title=Why%20Is%20My%20Classifier%20Discriminatory%3F%20In%3A%2032nd%20Conference%20on%20Neural%20Information%20Processing%20Systems%20%28NeurIPS%29&publication_year=2018&author=Chen%2CIY&author=Johansson%2CFD&author=Sontag%2CD)

[^81]: Haenssle HA, Fink C, Rosenberger A, Uhlmann L. Reply to “Man against machine: diagnostic performance of a deep learning convolutional neural network for dermoscopic melanoma recognition in comparison to 58 dermatologists” by H. A. Haenssle et al. Ann Oncol. 2019. [https://doi.org/10.1093/annonc/mdz015](https://doi.org/10.1093/annonc/mdz015)

[^82]: Ward-Peterson M, Acuña JM, Alkhalifah MK, Nasiri AM, Al-Akeel ES, Alkhaldi TM, et al. Association between race/ethnicity and survival of melanoma patients in the United States over 3 decades. Medicine. 2016;95:e3315. [https://doi.org/10.1097/md.0000000000003315](https://doi.org/10.1097/md.0000000000003315)

[Article](https://doi.org/10.1097%2Fmd.0000000000003315) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=27124020) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC4998683) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Association%20between%20race%2Fethnicity%20and%20survival%20of%20melanoma%20patients%20in%20the%20United%20States%20over%203%20decades&journal=Medicine.&doi=10.1097%2Fmd.0000000000003315&volume=95&publication_year=2016&author=Ward-Peterson%2CM&author=Acu%C3%B1a%2CJM&author=Alkhalifah%2CMK&author=Nasiri%2CAM&author=Al-Akeel%2CES&author=Alkhaldi%2CTM)

[^83]: Finlayson SG, Bowers JD, Ito J, Zittrain JL, Beam AL, Kohane IS. Adversarial attacks on medical machine learning. Science. 2019;363:1287–9.

[Article](https://doi.org/10.1126%2Fscience.aaw4399) [CAS](https://link.springer.com/articles/cas-redirect/1:CAS:528:DC%2BC1MXhtFCisr7M) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30898923) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC7657648) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Adversarial%20attacks%20on%20medical%20machine%20learning&journal=Science.&doi=10.1126%2Fscience.aaw4399&volume=363&pages=1287-1289&publication_year=2019&author=Finlayson%2CSG&author=Bowers%2CJD&author=Ito%2CJ&author=Zittrain%2CJL&author=Beam%2CAL&author=Kohane%2CIS)

[^84]: Mandel JC, Kreda DA, Mandl KD, Kohane IS, Ramoni RB. SMART on FHIR: a standards-based, interoperable apps platform for electronic health records. J Am Med Inform Assoc. 2016;23:899–908.

[Article](https://doi.org/10.1093%2Fjamia%2Focv189) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=26911829) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC4997036) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=SMART%20on%20FHIR%3A%20a%20standards-based%2C%20interoperable%20apps%20platform%20for%20electronic%20health%20records&journal=J%20Am%20Med%20Inform%20Assoc&doi=10.1093%2Fjamia%2Focv189&volume=23&pages=899-908&publication_year=2016&author=Mandel%2CJC&author=Kreda%2CDA&author=Mandl%2CKD&author=Kohane%2CIS&author=Ramoni%2CRB)

[^85]: Hersh WR, Weiner MG, Embi PJ, Logan JR, Payne PRO, Bernstam EV, et al. Caveats for the use of operational electronic health record data in comparative effectiveness research. Med Care. 2013;51(8 Suppl 3):S30–7.

[Article](https://doi.org/10.1097%2FMLR.0b013e31829b1dbd) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=23774517) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3748381) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Caveats%20for%20the%20use%20of%20operational%20electronic%20health%20record%20data%20in%20comparative%20effectiveness%20research&journal=Med%20Care&doi=10.1097%2FMLR.0b013e31829b1dbd&volume=51&issue=8%20Suppl%203&pages=S30-S37&publication_year=2013&author=Hersh%2CWR&author=Weiner%2CMG&author=Embi%2CPJ&author=Logan%2CJR&author=Payne%2CPRO&author=Bernstam%2CEV)

[^86]: Food and Drug Administration. Proposed Regulatory Framework for Modifications to Artificial Intelligence/Machine Learning (AI/ML)-Based Software as a Medical Device (SaMD): FDA; 2019. [https://www.regulations.gov/document?D=FDA-2019-N-1185-0001](https://www.regulations.gov/document?D=FDA-2019-N-1185-0001). Accessed 1 May 2019.

[^87]: Core MG, Lane HC, van Lent M, Gomboc D, Solomon S, Rosenberg M. Building Explainable Artificial Intelligence Systems. IAAI'06 Proceedings of the 18th conference on Innovative Applications of Artificial Intelligence. Volume 2; 2006. p. 1766–73.

[Google Scholar](http://scholar.google.com/scholar_lookup?&title=Building%20Explainable%20Artificial%20Intelligence%20Systems.%20IAAI%2706%20Proceedings%20of%20the%2018th%20conference%20on%20Innovative%20Applications%20of%20Artificial%20Intelligence.%20Volume%202&pages=1766-1773&publication_year=2006&author=Core%2CMG&author=Lane%2CHC&author=Lent%2CM&author=Gomboc%2CD&author=Solomon%2CS&author=Rosenberg%2CM)

[^88]: Holzinger A, Biemann C, Pattichis CS. What do we need to build explainable AI systems for the medical domain? arXiv. 2017; [https://arxiv.org/abs/1712.09923](https://arxiv.org/abs/1712.09923). Accessed 1 May 2019.

[^89]: Samek W, Wiegand T, Müller K-R. Explainable artificial intelligence: understanding, visualizing and interpreting deep learning models. arXiv. 2017; [http://arxiv.org/abs/1708.08296](http://arxiv.org/abs/1708.08296). Accessed 1 May 2019.

[^90]: Bologna G, Hayashi Y. Characterization of symbolic rules embedded in deep DIMLP networks: a challenge to transparency of deep learning. J Art Intel Soft Comput Res. 2017;7(4):265–86. [https://doi.org/10.1515/jaiscr-2017-0019](https://doi.org/10.1515/jaiscr-2017-0019)

[Article](https://doi.org/10.1515%2Fjaiscr-2017-0019) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Characterization%20of%20symbolic%20rules%20embedded%20in%20deep%20DIMLP%20networks%3A%20a%20challenge%20to%20transparency%20of%20deep%20learning&journal=J%20Art%20Intel%20Soft%20Comput%20Res&doi=10.1515%2Fjaiscr-2017-0019&volume=7&issue=4&pages=265-286&publication_year=2017&author=Bologna%2CG&author=Hayashi%2CY)

[^91]: Fox J. A short account of Knowledge Engineering. Knowl Eng Rev. 1984;1:4–14. [https://doi.org/10.1017/s0269888900000424](https://doi.org/10.1017/s0269888900000424)

[Article](https://doi.org/10.1017%2Fs0269888900000424) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=A%20short%20account%20of%20Knowledge%20Engineering&journal=Knowl%20Eng%20Rev&doi=10.1017%2Fs0269888900000424&volume=1&pages=4-14&publication_year=1984&author=Fox%2CJ)

[^92]: Lacave C, Díez FJ. A review of explanation methods for Bayesian networks. Knowl Eng Rev. 2002;17:107–27. [https://doi.org/10.1017/s026988890200019x](https://doi.org/10.1017/s026988890200019x)

[Article](https://doi.org/10.1017%2Fs026988890200019x) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=A%20review%20of%20explanation%20methods%20for%20Bayesian%20networks&journal=Knowl%20Eng%20Rev&doi=10.1017%2Fs026988890200019x&volume=17&pages=107-127&publication_year=2002&author=Lacave%2CC&author=D%C3%ADez%2CFJ)

[^93]: Doshi-Velez F, Kim B. Towards a rigorous science of interpretable machine learning. arXiv. 2017; [http://arxiv.org/abs/1702.08608](http://arxiv.org/abs/1702.08608). Accessed 1 May 2019.

[^94]: Lehman CD, Wellman RD, Buist DSM, Kerlikowske K, Tosteson ANA, Miglioretti DL, et al. Diagnostic accuracy of digital screening mammography with and without computer-aided detection. JAMA Intern Med. 2015;175:1828–37.

[Article](https://doi.org/10.1001%2Fjamainternmed.2015.5231) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=26414882) [PubMed Central](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC4836172) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Diagnostic%20accuracy%20of%20digital%20screening%20mammography%20with%20and%20without%20computer-aided%20detection&journal=JAMA%20Intern%20Med&doi=10.1001%2Fjamainternmed.2015.5231&volume=175&pages=1828-1837&publication_year=2015&author=Lehman%2CCD&author=Wellman%2CRD&author=Buist%2CDSM&author=Kerlikowske%2CK&author=Tosteson%2CANA&author=Miglioretti%2CDL)

[^95]: Phansalkar S, van der Sijs H, Tucker AD, Desai AA, Bell DS, Teich JM, et al. Drug-drug interactions that should be non-interruptive in order to reduce alert fatigue in electronic health records. J Am Med Inform Assoc. 2013;20:489–93.

[Article](https://doi.org/10.1136%2Famiajnl-2012-001089) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=23011124) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Drug-drug%20interactions%20that%20should%20be%20non-interruptive%20in%20order%20to%20reduce%20alert%20fatigue%20in%20electronic%20health%20records&journal=J%20Am%20Med%20Inform%20Assoc&doi=10.1136%2Famiajnl-2012-001089&volume=20&pages=489-493&publication_year=2013&author=Phansalkar%2CS&author=Sijs%2CH&author=Tucker%2CAD&author=Desai%2CAA&author=Bell%2CDS&author=Teich%2CJM)

[^96]: Sayres R, Taly A, Rahimy E, Blumer K, Coz D, Hammel N, et al. Using a deep learning algorithm and integrated gradients explanation to assist grading for diabetic retinopathy. Ophthalmology. 2019;126:552–64.

[Article](https://doi.org/10.1016%2Fj.ophtha.2018.11.016) [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&dopt=Abstract&list_uids=30553900) [Google Scholar](http://scholar.google.com/scholar_lookup?&title=Using%20a%20deep%20learning%20algorithm%20and%20integrated%20gradients%20explanation%20to%20assist%20grading%20for%20diabetic%20retinopathy&journal=Ophthalmology.&doi=10.1016%2Fj.ophtha.2018.11.016&volume=126&pages=552-564&publication_year=2019&author=Sayres%2CR&author=Taly%2CA&author=Rahimy%2CE&author=Blumer%2CK&author=Coz%2CD&author=Hammel%2CN)

[^97]: Wang D, Khosla A, Gargeya R, Irshad H, Beck AH. Deep Learning for Identifying Metastatic Breast Cancer. 2016. [http://arxiv.org/abs/1606.05718](http://arxiv.org/abs/1606.05718). Accessed 28 Aug 2019.

[Google Scholar](http://scholar.google.com/scholar_lookup?&title=Deep%20Learning%20for%20Identifying%20Metastatic%20Breast%20Cancer&publication_year=2016&author=Wang%2CD&author=Khosla%2CA&author=Gargeya%2CR&author=Irshad%2CH&author=Beck%2CAH)

[^98]: Google. People and AI Guidebook. [https://pair.withgoogle.com/](https://pair.withgoogle.com/). Accessed 10 May 2019.