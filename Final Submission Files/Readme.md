🧬 DNA Sequence Classification (CNN–BiLSTM)

This project implements a hybrid CNN–BiLSTM model to classify DNA splice junctions into:

EI (Exon–Intron)
IE (Intron–Exon)
N (Non-splice)

It also compares performance on encoded vs raw DNA datasets.

⚙️ How It Works
Old dataset → reshaped encoded features (60,3)
New dataset → one-hot encoded sequences (400,4)

Model:

CNN → learns local nucleotide patterns
BiLSTM → captures sequence dependencies
Output → 3-class classification
📊 Results
Dataset	Accuracy
Old (Encoded)	94.04%
New (Raw DNA)	90.50%
🚀 How to Run

Install dependencies:

pip install numpy pandas scikit-learn tensorflow datasets

👉 Recommended:
Run the project on Google Colab with GPU (A100 or similar) instead of a local Jupyter Notebook for faster training.

Go to: Runtime → Change runtime type → GPU
Select A100 / T4 / High-RAM GPU

Then run the notebook or script.

⚠️ Notes
Raw DNA dataset is more complex → slight accuracy drop is expected
Ensure correct label mapping between datasets
Training on CPU will be slow — GPU strongly recommended
🏁 Summary

The CNN–BiLSTM model effectively learns both local patterns and sequence dependencies, achieving strong performance and better generalization on real-world DNA data.
