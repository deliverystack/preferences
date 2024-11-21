
# Understanding the Differences Between `awk` and `sed`

## **Overview**

`awk` and `sed` are powerful text-processing tools in Unix-like operating systems, but they are designed with different use cases in mind.

### **Purpose**:
- **`sed`**: A **stream editor** focused on line-by-line text transformations. It's primarily used for text substitution, deletion, and pattern-based manipulation.
- **`awk`**: A **text processing language** designed for data extraction and reporting. It works on structured data, often treating text as fields and records.

### **Syntax**:
- **`sed`**: Has a concise and cryptic syntax suited for inline text editing.
- **`awk`**: Uses a more expressive syntax and supports variables, functions, and conditional statements, making it more like a programming language.

---

## **Why Both Exist**

- **Historical Context**: `sed` and `awk` were developed as part of the Unix philosophy of small, focused tools that do one thing well.
- **Complementary Functionality**: They address different needs. `sed` excels at simple text manipulation, while `awk` shines in data analysis and more complex tasks.

---

## **Advantages and Disadvantages**

| Feature             | `sed`                                   | `awk`                                  |
|---------------------|-----------------------------------------|---------------------------------------|
| **Advantages**      | - Lightweight and fast for simple tasks.<br>- Perfect for in-place file editing.<br>- Ideal for stream processing. | - Flexible, with built-in functions.<br>- Handles structured data.<br>- Better for complex logic. |
| **Disadvantages**   | - Limited to line-based operations.<br>- Poor for field-based data. | - Heavier for simple tasks.<br>- Overhead for in-place edits. |

---

## **What Each Can Do That the Other Cannot**

### **`sed`**:
- In-place editing of files (e.g., `sed -i` for direct substitution in a file).
- Handles multi-line transformations more naturally (e.g., `N` command to merge lines).
- Works as a pure stream editor without requiring structured data.

### **`awk`**:
- Handles structured data with field-based processing (`$1`, `$2`, etc.).
- Performs arithmetic operations, logical conditions, and string functions.
- Supports loops (`for`, `while`) and more complex control flow.

---

## **When They Can Be Used for the Same Purpose**

Both tools can be used for simple line-based pattern matching and text replacement:

- **Pattern Matching**:
  ```bash
  sed 's/foo/bar/g' file
  ```

  ```bash
  awk '{gsub(/foo/, "bar"); print}' file
  ```

- **Field Extraction** (though `awk` is better suited):
  ```bash
  sed 's/.*\(<field_pattern>\).*/\1/' file
  ```

  ```bash
  awk '{print $2}' file
  ```

---

## **When Each is Appropriate**

- **`sed`**:
  - Simple, line-by-line transformations.
  - One-liner substitutions and deletions.
  - In-place edits on large files without complex logic.

- **`awk`**:
  - Processing tabular or structured data (e.g., CSV, TSV).
  - Complex operations involving fields, conditions, and summaries.
  - Generating reports or formatted output.

---

## **Related Commands**

- **[`grep`](https://man7.org/linux/man-pages/man1/grep.1.html)**: A pattern-matching tool for extracting lines that match a regex. Simpler than both `awk` and `sed` but useful for filtering.
- **[`cut`](https://man7.org/linux/man-pages/man1/cut.1.html)**: Extracts fields or columns from delimited text. Similar to `awk` but with less flexibility.
- **[`sort`](https://man7.org/linux/man-pages/man1/sort.1.html)**: Sorts lines in a file. Often used in conjunction with `awk` for preprocessing data.
- **[`uniq`](https://man7.org/linux/man-pages/man1/uniq.1.html)**: Removes duplicate lines from sorted data.
- **[`tr`](https://man7.org/linux/man-pages/man1/tr.1.html)**: Translates or deletes characters in a stream.

---

## **Examples**

### 1. Simple Substitution
- Replace "foo" with "bar" in a file:
  ```bash
  sed 's/foo/bar/g' file
  ```
  ```bash
  awk '{gsub(/foo/, "bar"); print}' file
  ```

### 2. Extract Second Column from a CSV
- Using `awk`:
  ```bash
  awk -F, '{print $2}' file.csv
  ```

### 3. Delete Lines Containing a Pattern
- Using `sed`:
  ```bash
  sed '/pattern/d' file
  ```

- Using `awk`:
  ```bash
  awk '!/pattern/' file
  ```

### 4. Summing Numbers in a File
- Using `awk`:
  ```bash
  awk '{sum += $1} END {print sum}' file
  ```

### 5. Replace a Specific Field in Structured Data
- Using `awk`:
  ```bash
  awk -F, 'BEGIN {OFS=","} {$2 = "new_value"; print}' file.csv
  ```

---

## **Summary of Use Cases**

| Task                                    | Recommended Tool         | Explanation                                                                 |
|-----------------------------------------|--------------------------|-----------------------------------------------------------------------------|
| Simple text replacement                 | `sed`                   | Lightweight and fast for substitutions.                                     |
| In-place file editing                   | `sed`                   | Supports direct modifications with `-i`.                                   |
| Extracting and processing structured data | `awk`                   | Field-based processing with better control.                                |
| Data summarization (e.g., sum, avg)     | `awk`                   | Built-in arithmetic and functions.                                         |
| Multi-line text manipulation            | `sed`                   | Natural handling of streams for line joining.                              |
| Complex logic and formatted output      | `awk`                   | Full language features for flexibility.                                    |

Choosing between the two depends on the complexity of the task, the structure of the input, and performance considerations.


# Common Use Cases for `sed` and `awk`

This document provides examples of using `sed` and `awk` for text processing tasks.

---

## **1. Substituting Text**

### Using `sed`
Replace "old_text" with "new_text" in a file:
```bash
sed 's/old_text/new_text/g' file.txt
```

### Using `awk`
```bash
awk '{gsub(/old_text/, "new_text"); print}' file.txt
```

---

## **2. Deleting Lines**

### Using `sed`
Delete lines containing the pattern "unwanted":
```bash
sed '/unwanted/d' file.txt
```

### Using `awk`
```bash
awk '!/unwanted/' file.txt
```

---

## **3. Extracting Columns from a CSV**

### Using `awk`
Extract the second column from a comma-separated file:
```bash
awk -F, '{print $2}' file.csv
```

---

## **4. Appending Text After a Pattern**

### Using `sed`
Append "extra_text" after each line containing "pattern":
```bash
sed '/pattern/a extra_text' file.txt
```

### Using `awk`
```bash
awk '/pattern/ {print; print "extra_text"; next} 1' file.txt
```

---

## **5. Summing Numbers in a File**

### Using `awk`
Compute the sum of the numbers in the first column:
```bash
awk '{sum += $1} END {print sum}' numbers.txt
```

---

## **6. Replacing Specific Fields in Structured Data**

### Using `awk`
Replace the second field in a comma-separated file:
```bash
awk -F, 'BEGIN {OFS=","} {$2 = "new_value"; print}' file.csv
```

---

## **7. Counting Occurrences of a Pattern**

### Using `sed`
Count occurrences of "pattern":
```bash
sed -n '/pattern/p' file.txt | wc -l
```

### Using `awk`
```bash
awk '/pattern/ {count++} END {print count}' file.txt
```

---

## **8. Printing Lines Matching a Pattern**

### Using `sed`
Print lines containing "target":
```bash
sed -n '/target/p' file.txt
```

### Using `awk`
```bash
awk '/target/' file.txt
```

---

## **9. Reversing Lines in a File**

### Using `sed`
Reverse the order of lines (GNU `sed`):
```bash
sed '1!G;h;$!d' file.txt
```

### Using `awk`
```bash
awk '{line[NR] = $0} END {for (i = NR; i > 0; i--) print line[i]}' file.txt
```

---

## **10. Inserting Line Numbers**

### Using `awk`
Add line numbers to each line in a file:
```bash
awk '{print NR, $0}' file.txt
```

---

## **11. Finding and Replacing Multiple Patterns**

### Using `sed`
Replace "foo" with "bar" and "baz" with "qux":
```bash
sed -e 's/foo/bar/g' -e 's/baz/qux/g' file.txt
```

### Using `awk`
```bash
awk '{gsub(/foo/, "bar"); gsub(/baz/, "qux"); print}' file.txt
```

---

## **12. Filtering Lines Based on Length**

### Using `awk`
Print lines longer than 50 characters:
```bash
awk 'length($0) > 50' file.txt
```

---

## **13. Capitalizing the First Letter of Each Word**

### Using `awk`
```bash
awk '{for (i=1; i<=NF; i++) $i = toupper(substr($i, 1, 1)) tolower(substr($i, 2)); print}' file.txt
```

---

## **14. Duplicating Lines Based on a Condition**

### Using `awk`
Duplicate lines containing "important":
```bash
awk '/important/ {print; print} 1' file.txt
```

---

## **15. Extracting the First and Last Lines**

### Using `awk`
Print the first and last lines of a file:
```bash
awk 'NR == 1; END {print}' file.txt
```

---

These examples highlight some of the most common use cases for `sed` and `awk`. Use the tool that best fits your requirements based on the complexity of the task and the structure of the input data.

- [Bash Command Cheat Sheet](https://github.com/deliverystack/preferences/blob/main/bashcommands.md)
- [ChatGPT thread](https://chatgpt.com/share/673fa582-3d7c-8005-8635-8efc0e7648e9)

