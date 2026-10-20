# Automobile Sales Data Cleaning 

**Final Status: 0 Nulls, 0 Duplicates, 0 Infinity - 100% Clean**

### Raw Data Issues
- 1102 Nulls in TERRITORY, 104 in POSTALCODE, 28 in DEALSIZE
- SALES column was String like $2,871
- 27 Duplicate Rows

### Cleaning Steps
1. Fixed SALES: `replace('[\$,]','', regex=True).astype(float)`
2. Filled Nulls: `Unknown`, `mode()`, and `pd.qcut` logic for DEALSIZE
3. Removed Duplicates & Checked Infinity: `np.isinf`

### Final Result
Shape: (2824, 25)
Duplicates: 0
Infinity: 0
Nulls: 0

### Tools
Python, Pandas, NumPy, VS Code

Author: Syed Shees Kalam
