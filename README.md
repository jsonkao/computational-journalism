# Frontiers of Computational Journalism by Jonathan Stray
http://www.compjournalism.com/

_Reporting on society, using computation, and reporting on computation in society._

## High Dimensional Data

Vector-izing data, then projecting it into K << R (typically K=2 or K=3)

**Text analysis in Journalism**
- Clustering, classification
- Document Vector Space Model: what is this document about?
  - finding important words, topic analysis, key component for filtering
  - features = words works fine. One dimension = vocabulary of a document, value of a dimension = # of times word appears
    - Each entry becomes term frequency: tf(t,d)
  - distance metric for text (how similar? clustering?)
    - Looking for overlapping terms: Cosine similarity. similary(a,b) = (a \dot b) / (mag(a) \times mag(b)) = cos(theta). Cosine distance is just 1 - similarity(a,b).
  - also ignore stopwords and "de-weight" common words (e.g. "car" in car reviews). Document frequency `df(t,D)` = fraction of docs containing term
    - Inverse document frequency idf(t, D) = log(|D| / |d \in D : t \in d|)
  - [TF-IDF](https://planspace.org/20150524-tfidf_is_about_what_matters/) = tf(t,d) * idf(d, D) = term frequency * 1 / document frequency
