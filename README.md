"# deployment-01" 
# 1. Import Libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# 2. Load Your Dataset
df = pd.read_csv('path/to/your/d6ebc7f9-c811-4916-b5cc-e14bffb0e176.csv')  # Update path if needed
print("Shape of data:", df.shape)
df.head()

# 3. Basic Info
print("\nDataset Info:")
print(df.info())

print("\nMissing Values:")
print(df.isnull().sum())

# 4. Summary Statistics
print("\nSummary Stats:")
print(df.describe())

# 5. Visualize Distributions (for numerical columns)
df.hist(bins=30, figsize=(12, 10))
plt.tight_layout()
plt.show()

# 6. Correlation Heatmap
plt.figure(figsize=(10, 8))
sns.heatmap(df.corr(numeric_only=True), annot=True, cmap='coolwarm')
plt.title("Correlation Heatmap")
plt.show()

