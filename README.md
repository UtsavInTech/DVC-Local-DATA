# DVC-Local-DATA

This repository demonstrates the **basic working of Data Version Control (DVC)** using **local storage instead of cloud services (e.g., AWS S3)**.

The main objective of this project is to understand the **core concepts of DVC**, how it integrates with Git, and how data can be versioned efficiently in an MLOps workflow.


## Project Objective

- Learn how DVC works with Git
- Track data files using DVC
- Store versioned data locally (simulating an S3-like remote)
- Understand basic DVC commands and workflow
- Prepare a foundation for building an end-to-end ML pipeline


## Project Structure
DVC-local_Data/
│
├── data/                  # Directory containing data tracked by DVC
├── data.dvc               # DVC tracking file for data directory
├── s3/                    # Local directory used as DVC remote storage
├── mycode.py              # Simple Python script to generate CSV data
├── sample_data.csv        # Sample dataset for understanding data versioning
├── README.md              # Project documentation
├── LICENSE                # MIT License
└── .gitignore             # Ignored files (venv, cache, etc.)

## Technologies Used

- Python
- Git
- DVC
- Pandas
- Local filesystem as DVC remote

##  DVC Workflow Used in This Project

```bash
# Initialize DVC
dvc init

# Add data for versioning
dvc add data/

# Commit DVC metadata
git add data.dvc .gitignore
git commit -m "Track data using DVC"

# Add local directory as DVC remote
dvc remote add -d localstorage s3/

# Push data to DVC remote
dvc push

# Pull data from DVC remote
dvc pull
Purpose of This Repository

This project is created purely for learning purposes to build a strong foundation in:
	•	Data versioning
	•	Reproducible ML workflows
	•	MLOps fundamentals

It intentionally avoids cloud services to keep the focus on understanding DVC concepts clearly.
Future Work
	•	Create a DVC pipeline using dvc.yaml
	•	Add data preprocessing stage
	•	Add model training and evaluation stages
	•	Track metrics and experiments
	•	Convert this into an end-to-end ML pipeline

⸻

License

This project is licensed under the MIT License.
