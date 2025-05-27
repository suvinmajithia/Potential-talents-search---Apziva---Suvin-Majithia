Intelligent Candidate Fit Ranking with BERT & Doc2Vec
Semantic Similarity-Based Talent Matching for Tech Roles

🚀 Overview
This project builds an intelligent ranking system to identify the best-fit candidates for a given role by computing semantic similarity between candidate job titles and role-specific keywords. It combines BERT and Doc2Vec embeddings with Cosine Similarity to quantify fit, and uses user feedback (starring) to iteratively improve results.

🧠 Objective
Predict and rank candidate fitness for a role based on job title semantics, using keyword matching via vector similarity. Re-rank when a user provides feedback on the most relevant candidates.

🛠 Technologies Used
Python
BERT (Transformers)
Doc2Vec (Gensim)
Cosine Similarity (sklearn)
Pandas / NumPy
Jupyter Notebook

🧬 Methodology
1. Preprocessing: 
- Clean and tokenize job titles.
2. Embeddings:
- Generate job title embeddings using BERT and Doc2Vec.
- Generate keyword embeddings using same techniques.
3. Similarity Scoring:
- Compute cosine similarity between job titles and keywords.
- Apply weighted average of BERT and Doc2Vec scores based on user-defined preference.
4. Ranking:
- Candidates sorted in descending order of weighted score.
- User can “⭐ star” candidates to re-rank list using this supervised feedback.
5. Re-Ranking Logic:
- After starring, the ideal candidate vector is used to re-score remaining candidates based on vector proximity.

📊 Dataset
Source: Internal talent sourcing dataset (anonymized)
Attributes:
id: Unique candidate ID
job_title: Text
location: Candidate location
connections: Number of professional connections
fit: Target label (float 0-1, optional)

✅ Goals
1. Rank candidates based on similarity to keywords like "Aspiring human resources".
2. Dynamically re-rank based on starred (preferred) candidates.
3. Enable thresholding and filtering of irrelevant candidates.
4. Reduce manual review time while enhancing match quality.

📈 Success Metrics
1. Initial ranking quality (semantic match accuracy).
2. Improvement after starring (list convergence).
3. Cut-off threshold effectiveness (filtering irrelevant candidates).
4. Reduction in manual effort.

🔁 Future Extensions
1. Build interactive dashboard for sourcing teams.
2. Integrate LinkedIn scraping (compliant with TOS).
3. Apply clustering for candidate segmentation.
4. Use fine-tuned domain-specific BERT models (e.g., JobBERT).
