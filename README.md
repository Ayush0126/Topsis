---

# **Topsis-Ayush-102203119**

A Python package for implementing the Technique for Order of Preference by Similarity to Ideal Solution (TOPSIS) method. This method is used for multi-criteria decision-making.

---

## **Installation**

Install the package using `pip`:

```bash
pip install Topsis-Ayush-102203119
```

---

## **Usage**

### **Command-Line Interface**

After installation, you can use the `topsis` command to calculate rankings for your dataset.

#### **Command Syntax**
```bash
topsis <InputDataFile> <Weights> <Impacts> <ResultFileName>
```

- `<InputDataFile>`: Path to the input CSV file.
- `<Weights>`: Comma-separated list of weights for each criterion (e.g., `1,1,1,2`).
- `<Impacts>`: Comma-separated list of impacts for each criterion (`+` for positive, `-` for negative).
- `<ResultFileName>`: Path to save the output CSV file.

---

### **Input File Format**
- The input file must be a CSV with at least 3 columns.
- The **first column** should contain the names of the objects (e.g., M1, M2, ...).
- The remaining columns should contain **numeric criteria values**.

#### Example Input (`data.csv`):
```csv
Object,Criteria1,Criteria2,Criteria3,Criteria4
M1,250,16,12,5
M2,200,16,8,3
M3,300,32,16,4
M4,275,16,8,4
M5,225,32,16,2
```

---

### **Example Usage**
1. Prepare the input CSV file (e.g., `data.csv`).
2. Run the following command:

```bash
topsis data.csv 1,1,1,2 +,+,-,+ result.csv
```

3. The result will be saved in the specified output file (e.g., `result.csv`).

#### Example Output (`result.csv`):
```csv
Object,Criteria1,Criteria2,Criteria3,Criteria4,Topsis Score,Rank
M1,250,16,12,5,0.75,2
M2,200,16,8,3,0.45,4
M3,300,32,16,4,0.85,1
M4,275,16,8,4,0.55,3
M5,225,32,16,2,0.30,5
```

---

## **Requirements**

This package requires the following Python libraries:
- `numpy`
- `pandas`

These dependencies are automatically installed with the package.

---

## **License**

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

