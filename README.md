# Cancer Type Detection on Hispathological Data using Multi-Instance Learning
This repo contains a response to the Owkin proposal for 2023 ENS Data Challenges : **Detecting PIK3CA mutation in breast cancer**.

**PIK3CA mutation in breast cancer**  

Recent studies have also shown that histopathology slides contain information that underlie tumor genotype, therefore they can be used to predict genomic alterations such as point mutations. One of the genomic alterations that is particularly interesting is PIK3CA mutation in breast cancer. They occur in around 30%-40% of breast cancer and are most commonly found in estrogen receptor-positive breast cancer. PIK3CA mutations have been associated with good outcomes. More importantly, patients who carry these mutations and are resistant to endocrine therapy may respond to a class of target therapy - the PI3Kα inhibitor.

**Challenge's purpose**  

Current method for identifying PIK3CA mutations is DNA sequencing, which requires technical and bioinformatic expertise that is not accessible in all laboratories. An automated solution to detect PIK3CA mutation has high clinical relevance as it could provide a fast, reliable screening tool allowing more patients, especially in tertiary centers, to be eligible to personalized therapies associated to better outcomes.

**Challenge's goal**  

The challenge proposed by Owkin is a weakly-supervised binary classification problem. Weak supervision is crucial in digital pathology due to the extremely large dimensions of whole-slide images (WSIs), which cannot be processed as is. To use standard machine learning algorithms one needs, for each slide, to extract smaller images (called tiles) of size 224x224 pixels (approx 112 µm²). Since a slide is given a single binary annotation (presence or absence of mutation) and is mapped to a bag of tiles, one must learn a function that maps multiple items to a single global label. This framework is known as multiple-instance learning (MIL). More precisely, if one of the pooled tiles exhibits a mutation pattern, presence of mutation is predicted while if none of the tiles exhibit the pattern, absence of mutation is predicted. This approach alleviates the burden of obtaining locally annotated tiles, which can be costly or impractical for pathologists.
