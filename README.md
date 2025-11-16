# Document Similarity Analysis using Vector Space Model

A comprehensive implementation of document similarity analysis using TF-IDF (Term Frequency-Inverse Document Frequency) and cosine similarity metrics.

## 📋 Overview

This project implements a document similarity analysis system that:
- Collects and processes multiple text documents
- Calculates TF-IDF vectors for each document
- Computes cosine similarity between document pairs
- Visualizes similarity matrix and provides insights
- Offers both web interface and Python implementation

## 🎯 Features

- **Document Collection**: Processes 5-10 documents from various sources
- **Vector Space Model**: Implements TF-IDF weighting scheme
- **Similarity Calculation**: Uses cosine similarity metric
- **Visualization**: Interactive heatmap of similarity scores
- **Export Functionality**: Download results in multiple formats
- **Web Interface**: User-friendly React-based interface

## 🚀 Quick Start

### Prerequisites
```bash
python 3.8+
numpy
pandas
scikit-learn
matplotlib
seaborn
```

### Installation
```bash
git clone https://github.com/yourusername/document-similarity.git
cd document-similarity
pip install -r requirements.txt
```

### Running the Analysis
```bash
python document_similarity.py
```

## 📊 Methodology

### 1. Text Preprocessing
- Convert text to lowercase
- Remove punctuation and special characters
- Tokenization
- Remove stopwords
- Stemming/Lemmatization (optional)

### 2. TF-IDF Calculation

**Term Frequency (TF)**:
```
TF(t, d) = (Number of times term t appears in document d) / (Total number of terms in document d)
```

**Inverse Document Frequency (IDF)**:
```
IDF(t) = log(Total number of documents / Number of documents containing term t)
```

**TF-IDF Weight**:
```
TF-IDF(t, d) = TF(t, d) × IDF(t)
```

### 3. Cosine Similarity

```
Similarity = cos(θ) = (A · B) / (||A|| × ||B||)
```

Where:
- A and B are TF-IDF vectors
- A · B is the dot product
- ||A|| and ||B|| are the magnitudes

## 📁 Project Structure

```
document-similarity/
├── README.md
├── requirements.txt
├── document_similarity.py      # Main Python implementation
├── documents/                  # Sample documents folder
│   ├── doc1.txt
│   ├── doc2.txt
│   ├── doc3.txt
│   ├── doc4.txt
│   └── doc5.txt
├── results/                    # Output folder
│   ├── similarity_matrix.csv
│   ├── heatmap.png
│   └── analysis_report.pdf
└── web_interface/              # React web app
    ├── src/
    └── package.json
```

## 💻 Code Examples

### Basic Usage
```python
from document_similarity import DocumentSimilarity

# Initialize analyzer
analyzer = DocumentSimilarity()

# Add documents
analyzer.add_document("doc1.txt")
analyzer.add_document("doc2.txt")

# Calculate similarities
similarity_matrix = analyzer.calculate_similarity_matrix()

# Visualize results
analyzer.plot_heatmap()
```

### Advanced Usage
```python
# Custom preprocessing
analyzer = DocumentSimilarity(
    use_stemming=True,
    min_df=2,
    max_df=0.8,
    ngram_range=(1, 2)
)

# Generate detailed report
analyzer.generate_report(output_path="results/report.pdf")
```

## 📈 Sample Results

### Similarity Matrix Example

|       | Doc 1 | Doc 2 | Doc 3 | Doc 4 | Doc 5 |
|-------|-------|-------|-------|-------|-------|
| Doc 1 | 1.000 | 0.745 | 0.123 | 0.678 | 0.089 |
| Doc 2 | 0.745 | 1.000 | 0.098 | 0.823 | 0.112 |
| Doc 3 | 0.123 | 0.098 | 1.000 | 0.156 | 0.734 |
| Doc 4 | 0.678 | 0.823 | 0.156 | 1.000 | 0.201 |
| Doc 5 | 0.089 | 0.112 | 0.734 | 0.201 | 1.000 |

### Key Findings
- Documents 2 and 4 show highest similarity (0.823)
- Documents 3 and 5 are moderately similar (0.734)
- Documents 1 and 5 show minimal similarity (0.089)

## 🔍 Document Sources

The sample documents are collected from:
1. **AI Overview** - Technology article on artificial intelligence
2. **Machine Learning Basics** - Educational content on ML fundamentals
3. **Climate Change Report** - Environmental science article
4. **Deep Learning Applications** - Technical documentation
5. **Renewable Energy** - Green technology article

## 📊 Visualizations

The system generates:
- **Heatmap**: Color-coded similarity matrix
- **Dendogram**: Hierarchical clustering of documents
- **Bar Charts**: Top similar document pairs
- **Word Clouds**: Key terms per document cluster

## 🛠️ Technologies Used

- **Python**: Core implementation
- **NumPy**: Numerical computations
- **scikit-learn**: TF-IDF vectorization
- **Pandas**: Data manipulation
- **Matplotlib/Seaborn**: Visualizations
- **React**: Web interface
- **Tailwind CSS**: Styling

## 📝 Report Sections

The generated report includes:
1. Introduction & Methodology
2. Document Descriptions
3. Preprocessing Steps
4. TF-IDF Calculation Details
5. Similarity Matrix
6. Visualization & Analysis
7. Key Findings & Conclusions
8. Code Snippets

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👤 Author
Aashish Adhikari

## 🙏 Acknowledgments

- scikit-learn documentation
- Vector Space Model research papers
- Information Retrieval textbooks

## 📧 Contact

For questions or feedback, please open an issue or contact aashishad67@gmail.com

---

**Note**: Replace placeholder URLs and contact information with your actual details before publishing.
