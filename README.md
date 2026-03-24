# Genomic Correlation Between Type 1 Diabetes and Severe Allergic Phenotypes in Underrepresented Populations


This project is driven by a personal connection to a loved one with Type 1 Diabetes (T1D). I intend to use this work to establish myself in the field, specifically focusing on the intersection of data science and social good.


My research has identified recurring themes of underrepresentation in the Black community, even as T1D rates increase. Black individuals with T1D are statistically more likely to experience ketoacidosis. Existing literature suggests this may be inclusive of several factors, including a lack of education regarding insulin pump usage among patients and caregivers. By combining my personal perspective, lived experience, and data science training, I aim to provide meaningful contributions to both the clinical and patient communities.


## Background and Literature Review
While extensive research exists regarding the relationship between T1D and celiac disease, few papers address my specific area of interest: the link between early-onset T1D and severe allergic reactions.
*	I was struck by a discussion regarding "big events" that trigger T1D from a dormant state to a progressive takeover of the pancreas. This aligns with a personal observation: after a severe anaphylactic reaction at age two, my brother was diagnosed with T1D three years later, despite initial medical dismissal.
*	Historically, T1D and allergies were considered "immunologically antagonistic" because (diabetes-related) and (allergy-related) cells are polarized, effectively pulling the immune system in different directions.
*	Recent studies (Smew et al., 2025) suggest the "inhibitory system" is an oversimplification. Strong associations have been found between T1D, asthma, allergic rhinitis, and eczema. While the correlation between asthma and T1D is well-established, results for eczema and rhinitis remain conflicting.


## Data Foundation and Infrastructure
To ensure this research is built on curated, high-confidence data, I utilize the following industry-standard tools:
*	__ClinVar and NCBI Ecosystem__: These act as the "bridge" between raw genetic data and clinical reality. ClinVar allows for the mapping of genetic variants to specific phenotypes, while NCBI’s MedGen standardizes these phenotypes using universal ontologies.
*	__GWAS Catalog__: This is utilized for mapping genotype-phenotype associations at a massive scale. It is crucial for demographic research, allowing for the integration of ancestral diversity to reduce health inequities and improve risk prediction accuracy across different populations.


## Methodology and LLM Integration
I plan to utilize Large Language Models (LLMs) to bridge the gap between disparate datasets and refine demographic filtering:
*	Data Joining: I will task the LLM with joining GWAS subset data with ClinVar subsets using RSID and chromosome + base pair positions. Following the __AutoDW__ framework (Liu et al., 2024), I will also use LLMs for __Feature Type Inference__ to identify "influential columns" within the standardized variant_summary.
*	Demographic Filtering: I am interested in using LLMs to find a middle ground for demographic filtering of GWAS ancestry data and to quantify the number of Black participants in specific studies.
*	Phenotype Labeling: I will explore if LLMs can help identify better phenotypes and genosymbols for labeling T1D and anaphylaxis. As highlighted by Zhou et al. (2025), I will use __Semantic Matching__ to resolve the current lack of overlap between datasets where rigid string filtering fails.
*	LLM Enhanced Data Preparation Framework: Following the end-to-end data wrangling solutions proposed in AutoDW (Liu et al., 2024), I will transition from manual string filtering to LLM-based feature type inference to better map the 43 variant columns. Furthermore, as highlighted by Zhou et al. (2025), I will utilize LLMs for 'Data Integration' to resolve the current lack of overlap between T1D and allergy subsets, ensuring that semantic similarities in phenotypes are not missed by rigid R-based filtering.


## Research Question and Hypothesis
What shared variants/loci exist between severe early-onset food allergy phenotypes and T1D, and are these loci underrepresented in Black populations within ClinVar?
While preliminary GWAS filtering yielded no overlapping variants , this is likely a representation issue or an artifact of rigid string-matching filters. Following the frameworks of Liu et al. (2024) and Zhou et al. (2025), the next phase of this project will utilize semantic LLM integration to bridge the gap between ClinVar and GWAS datasets, specifically searching for the shared loci identified in recent Swedish cohort studies (Smew et al., 2025). I expect to find a correlated relationship between early-onset severe allergic responses and the subsequent development of T1D, despite conflicting findings in current Genome-Wide Association Studies data and the Variant data.


## Summary of Planned Work
*	__Immediate Focus__: Extensive literature review to narrow focus (e.g., specific tree nut allergies) and investigate the development of new food allergies after the onset of T1D.
*	__Iterative Methodology__: Refine the research question and use LLMs to re-employ the EDA checklist with revised keywords for T1D and anaphylaxis.
*	__Validation and Quality Control__:
  *	Validate data against one external source.
  *	Create plots to identify missing data points in tables.
  *	Establish "Great Expectations" and check for data deviations.
*	__Follow-up Inquiries__:
  *Evaluate if the current focus on genomes and phenotypes is sufficient.
  *Refine the definition of anaphylaxis and determine if and can be filtered within this specific dataset.


## Citations
__Liu, L., et al.__ (2024). AutoDW: Automatic Data Wrangling Leveraging Large Language Models. In Proceedings of the 39th IEEE/ACM International Conference on Automated Software Engineering (pp. 2041–2052). 


__Smew, A. I., et al.__ (2025). Disentangling the comorbidity between allergic disease and type 1 diabetes using genetically informative designs. The Journal of Allergy and Clinical Immunology.


__Zheng, J., et al.__ (2025). Large language models for data science: A survey on readiness, benefits, and challenges. Data Science and Management, 8(1). 


__Zhou, W., et al.__) (2025). Can LLMs Clean Up Your Mess? A Survey of Application-Ready Data Preparation with LLMs. IEEE Transactions on Knowledge and Data Engineering (TKDE). 

