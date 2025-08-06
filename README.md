# Wildlife Movement Prediction Using Deep Learning

This project leverages deep learning techniques to model and predict the migratory movement of wildlife species using real-world geospatial telemetry data. We use data sourced from Movebank and apply GRU-based neural networks to model temporal movement patterns and predict future positions based on historical trajectories.

---

## 📁 Project Structure

- `Wildlife_Notebook.ipynb` – Main Jupyter notebook for preprocessing, EDA, modeling, and evaluation.
- `Wildlife_Notebook.html` – HTML export of the notebook for direct browser viewing (hosted on AWS).
- `test_predictions_with_errors.csv`, `migration_original.csv` – Cleaned datasets used for training/testing.

---

## 🔗 Hosted HTML Notebook

You can view the full notebook rendered as a webpage here:

👉 **[View HTML Notebook on AWS S3](https://aarjunwildlifenotebook.s3.ap-south-1.amazonaws.com/Wildlife_Notebook.html)**

---

## 📊 Data Source

- Source: [Movebank](https://www.movebank.org/)
- Dataset: Bird migration telemetry data.
- Features extracted:
  - Timestamp
  - Latitude / Longitude
  - Speed
  - Distance covered
  - Time delta between locations

---

## 🔍 Exploratory Data Analysis

The EDA phase covered:

- Visualizing geospatial trajectories
- Handling missing values and anomalies
- Calculating `distance(km)` and `speed(km/hr)`
- Generating `time_diff(hrs)` between observations
- Heatmaps, trajectory plots, and time-series inspection

---

## 🧠 Model Used – GRU (Gated Recurrent Unit)

We implemented a GRU-based deep learning model using PyTorch to model the temporal dependencies in the migration data. The pipeline includes:

- Sequence creation using sliding window
- Normalization of inputs
- Model architecture with GRU layers
- Training using MSE loss
- Validation using test set predictions
- Visual comparison of predicted vs. actual migration paths

---

## 📈 Training Details

- Loss Function: Mean Squared Error
- Optimizer: Adam
- Epochs: 100+
- Training/validation split: 80/20
- Batch size: 32
- Model evaluation using loss plots and test accuracy

---

## ☁️ AWS S3 Hosting

The final notebook has been exported to `.html` and hosted using **Amazon S3**:

- S3 Bucket Name: `aarjunwildlifenotebook`
- Region: `Asia Pacific (Mumbai)`
- Public Access enabled for HTML file
- Direct browser link available in this README

---

## 🛠 Tools & Technologies

- **Languages**: Python
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, PyTorch
- **Model**: GRU (Recurrent Neural Network)
- **Hosting**: AWS S3
- **IDE**: Jupyter Notebook (exported to HTML)

---

## 🧠 Author

**Aarjun Mahule**  
📧 [aarjun.mahule23@gmail.com](mailto:aarjun.mahule23@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/aarjunmahule23)  
💻 [GitHub](https://github.com/aarjunm04)

---

## 🚀 Future Improvements

- Live deployment using Streamlit or Flask
- More advanced architectures like LSTM + Attention
- Real-time tracking of tagged species using external APIs
