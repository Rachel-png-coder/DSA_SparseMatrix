Overview
This project implements memory-efficient sparse matrix operations in Python. It uses a Dictionary of Keys (DOK) format to store only non-zero elements, making it suitable for large sparsematrices      
Getting Started

Installation
Clone this repository:
git clone <https://github.com/Rachel-png-coder/DSA_SparseMatrix>
cd dsa/sparse_matrix
No additional installation needed - we only use standard Python!
📝 File Format
Input files must follow this format:

rows=<number>
cols=<number>
(row, col, value)
(row, col, value)
...
Example:

rows=8433
cols=3180
(0, 381, -694)
(0, 128, -838)
(0, 639, 857)
Format Rules
First line: rows=<positive integer>
Second line: cols=<positive integer>
Following lines: (row, col, value) where:
row must be between 0 and rows-1
col must be between 0 and cols-1
value must be an integer
Whitespace is ignored
All numbers must be integers
Usage
Run the program:
cd code/src
python main.py
Select an operation:
Sparse Matrix Operations
1. ➕ Add matrices
2. ➖ Subtract matrices
3. ✖️ Multiply matrices
4. 📊 Display matrix statistics
5. 👋 Exit
Choose input files:
Enter 1-3 for sample files
Or type a full path to your own file
Results will be saved in the results/ directory with timestamp
Implementation Details
Core Classes
SparseMatrix: Main class implementing sparse matrix operations
Uses Dictionary of Keys (DOK) format
Only stores non-zero elements
Optimized for memory efficiency
Key Operations
# Create from file
matrix = SparseMatrix("path/to/file.txt")

# Create empty
matrix = SparseMatrix(num_rows=10, num_cols=10)

# Get/Set elements
value = matrix.get_element(row, col)
matrix.set_element(row, col, value)

# Matrix operations
result = matrix1.add(matrix2)
result = matrix1.subtract(matrix2)
result = matrix1.multiply(matrix2)
Error Handling
The implementation handles various error cases:

Invalid file formats
Out-of-bounds indices
Incompatible matrix dimensions
Missing or unreadable files
Invalid number formats
🛠️ Matrix Operation Rules
Addition/Subtraction
Both matrices must have the same dimensions
Results in matrix of same size
Adds/subtracts corresponding elements
Multiplication
Matrix 1 columns must equal Matrix 2 rows
Results in matrix of size (M1_rows × M2_cols)
Uses efficient sparse multiplication algorithm
📈 Performance Considerations
Only stores non-zero elements
Optimized multiplication for sparse matrices
Efficient memory usage for large sparse matrices
Fast access to elements using dictionary
📄 License
This project is for educational purposes. Feel free to learn from it!


