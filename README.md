# MUJ-DS-2430010355
# PLOT2GENRE 
### Movie Genre Classification Using Plot Summaries

## 1. Project Overview

PLOT2GENRE is a deep-learning project that predicts a movie's primary genre using only its plot summary. It transforms textual descriptions into semantic embeddings and uses a Multi-Layer Perceptron (MLP) classifier to predict one of six movie genres.

The project demonstrates an end-to-end NLP and deep-learning workflow, from data collection and preprocessing to model training, evaluation, and interactive prediction.

## 2. Objectives

- Collect movie metadata and plot summaries using the TMDB API.
- Generate semantic text representations using a pretrained MiniLM sentence-transformer.
- Build a neural network for six-class genre classification.
- Study underfitting, overfitting, and the bias–variance trade-off.
- Apply regularization and early stopping.
- Evaluate generalization using stratified five-fold cross-validation and a held-out test set.

## 3. Genres Covered

- Action
- Adventure
- Animation
- Comedy
- Drama
- Horror

## 4. Technologies Used

- Python
- Google Colab
- PyTorch
- Sentence Transformers
- `all-MiniLM-L6-v2`
- Scikit-learn
- Pandas and NumPy
- Matplotlib and Seaborn
- TMDB API

## 5. Methodology

1. **Data collection:** Retrieve movie metadata and plot summaries from TMDB.
2. **Preprocessing:** Clean the data, select the primary genre, retain six genres, and create stratified data splits.
3. **Text representation:** Convert each plot summary into a 384-dimensional embedding using a frozen MiniLM encoder.
4. **Model development:** Train an MLP with the architecture 384 → 128 → 64 → 6.
5. **Regularization:** Apply dropout, weight decay, and early stopping.
6. **Model analysis:** Compare underfitting and overfitting experiments to study model complexity.
7. **Validation:** Perform stratified five-fold cross-validation.
8. **Evaluation:** Measure accuracy, precision, recall, macro F1, weighted F1, and confusion-matrix results.
9. **Prediction:** Use the trained classifier to predict genres for new plot summaries.

## 6. Reported Results

### Held-Out Test Set

| Metric | Result |
|---|---:|
| Accuracy | 57.96% |
| Macro Precision | 54.65% |
| Macro Recall | 52.25% |
| Macro F1-score | 51.45% |
| Weighted F1-score | 56.53% |

### Five-Fold Cross-Validation

| Metric | Mean ± Standard Deviation |
|---|---:|
| Accuracy | 55.77% ± 1.94% |
| Macro F1-score | 48.29% ± 1.56% |

These results provide a baseline for plot-summary-based genre classification and leave room for future improvements.

## 7. Repository Structure

- `README.md` — Project documentation
- `notebooks/` — Google Colab/Jupyter notebooks
- `code/` — Reusable source code
- `assignments/` — Course assignments
- `resources/` — Supporting resources and permitted datasets
- `presentations/` — Project presentations
- `capstone/` — Final capstone deliverables

## 8. How to Run

1. Open the project notebook in Google Colab.
2. Install the required Python dependencies specified in the notebook.
3. Provide a valid TMDB API Read Access Token when prompted.
4. Run the notebook cells in order to collect the data, preprocess it, train the model, and evaluate its performance.
5. Use the prediction and interactive demo sections to test movie plot summaries.

**Requirements:** Internet access for TMDB data collection and access to the pretrained sentence-transformer model. Google Drive is used for storing project outputs and the trained model.

## 9. Limitations and Future Improvements

- Improve classification performance across genres.
- Investigate class imbalance and genre-specific prediction errors.
- Experiment with alternative text representations and classifier architectures.
- Explore multi-label classification for movies that belong to multiple genres.
- Evaluate performance on additional or more diverse movie datasets.

## 10. Data and Model Notes

Movie metadata is obtained through The Movie Database (TMDB) API. Refer to [TMDB](https://www.themoviedb.org/) for its terms, attribution requirements, and data-use policies.

The project uses the pretrained `all-MiniLM-L6-v2` sentence-transformer to represent plot summaries.

## 11. Student Information

- **Name:** Gitanjali Juyal
- **Registration Number:** 2430010355
- **Branch:** Data Science
- **Batch:** E

## 12. Training Program

**Institution:** Manipal University Jaipur  
**Program:** Batch E
