<p align="center">
  <h1 align="center">🧹 DATA PREPROCESSING</h1>
</p>

---

## 📌 Overview

This project focuses on **data preprocessing**, a critical step in any data science or machine learning pipeline. The goal is to clean, transform, and prepare raw data to improve the quality of analysis or model performance.

---

## 🔍 Business Understanding

The objective is to obtain a well-structured time series dataset using the **P2.5** collection from the site or location that has the most data points.

---

## 🧠 Data Understanding

We are working with multiple databases hosted on a client server (MongoDB: `AieQuality`). These include:

- **Available Databases/Collections:**
  - Nairobi
  - Kisumu
  - Mombasa
  - Juja
  - Nakuru

- **Selected Collection:** Nairobi  
- **Total Documents in Nairobi:** `446,968`

- **Sample Document (First Entry):**

```json
{
  "_id": ObjectId("6806979f55fcce47f5780944"),
  "sensor_id": 4899,
  "sensor_type": "DHT22",
  "location": 3966,
  "lat": -1.311,
  "lon": 36.817,
  "timestamp": "2025-01-01T00:02:30.504000+00:00",
  "value_type": "humidity",
  "value": 74.5
}
```
- Final python code for the entire pipeline.
```python
import pandas as pd

def wrangle(collection):
    # Query documents from the collection
    result = collection.find(
        {"location": 3573, "value_type": "P2"},
        projection={"timestamp": 1, "value": 1, "_id": 0}
    )
    # Convert result into DataFrame
    df = pd.DataFrame(result).set_index("timestamp")
    # Convert timezone to 'Africa/Nairobi'
    df.index = df.index.tz_convert("Africa/Nairobi")
    return df
```
## 🛠️ Technologies & Libraries Used

| 🧩 Library             | 📌 Description                                |
|------------------------|----------------------------------------------|
| 🐍 **Python**          | Core programming language                     |
| 🐼 **Pandas**          | Data manipulation and analysis                |
| 📁 **Pathlib**         | Modern file system path handling              |
| 🍃 **PyMongo**         | MongoDB database access from Python           |
| 🌍 **Pytz**            | Timezone-aware datetime conversions           |
| 🧪 **Scikit-learn**    | Preprocessing tools & ML utilities            |
| 🖨️ **PrettyPrinter**   | Clean and readable console output of data     |


---
