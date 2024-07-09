# Intermidiate Unix CLI

## sort

### Sort Alphabetically by Name
```bash
    sort employees.txt

```

### Sort in Reverse Alphabetical Order by Name

```bash
    sort -r employees.txt
```

### Sort Numerically by Salary (3rd Column)

```bash
    sort -t ',' -k 3 -n employees.txt
```

### Sort by Department and Then by Salary Within Each Department

```bash
    sort -t ',' -k 2,2 -k 3,3n employees.txt
```
- -t ',': Sets the delimiter to a comma.

### Case-Insensitive Sort:

```bash
    sort -f employees.txt
```
- -f: Ignores case differences when sorting.

### Remove Duplicate Lines:

```bash
    sort -u employees.txt
```
- -u: Removes duplicate lines after sorting.

## grep

### Search for a Specific String

```bash
    grep "ERROR" log.txt
```
### Case-Insensitive Search:

```bash
    grep -i "error" log.txt
```
- Finds all lines containing "error", ignoring case differences

### Display Line Numbers

```bash
    grep -n "jdoe" log.txt
```
- Finds all lines containing "jdoe" and displays line numbers

### Search for Multiple Patterns

```bash
    grep -E "ERROR|WARNING" log.txt
```
- Finds all lines containing either "ERROR" or "WARNING"

### Invert Match

```bash
    grep -v "INFO" log.txt
```
- Finds all lines that do not contain "INFO".

### Count Matches
```
    grep -c "jdoe" log.txt
```
### Display Only Matching Parts

```bash
    grep -o "user: [a-z]*" log.txt
```


# sed

### Substitute Text:

- Replace first occurrence of "Marketing" with "Sales":
    ```bash
    sed 's/Marketing/Sales/' data.txt
    ```
- Replace all occurrences of "IT" with "Information Technology":
    ```bash
    sed 's/IT/Information Technology/g' data.txt
    ```

### Substitute Text In-Place:

- Replace all occurrences of "Accounting" with "Finance" and save changes:
    ```bash
    sed -i 's/Accounting/Finance/g' data.txt
    ```

### Delete Lines:

- Delete lines containing "Marketing":
    ```bash
    sed '/Marketing/d' data.txt
    ```
- Delete line 3:
    ```bash
    sed '3d' data.txt
    ```
### Insert Lines

- Insert a line before line 2:
    ```bash
    sed '2i\New Employee, New Department, 5000' data.txt
    ```
- Append a line after line 4:
    ```bash
    sed '4a\New Employee, New Department, 5000' data.txt
    ```
### Print Specific lines
- print line 2
    ```bash
    sed -n '2p' data.txt
    ```

- Print lines 2 to 4
    ```bash
    sed -n '2,4p' data.txt
    ```
### Print Lines Matching a Pattern:
```bash
    sed -n '/IT/p' data.txt
```

## awk

### Print Specific Columns

- Print the First Column (Names)

    ```bash
    awk '{print $1}' data.txt
    ```
- Print the First and Third Columns (Names and Salaries)
    ```bash
    awk '{print $1, $3}' data.txt
    ```

### Print Lines Matching a Pattern
- Print lines where the department is "IT":
    ```bash
    awk '$2 == "IT"' data.txt
    ```

### Perform Calculations on Fields:

- Calculate the total salary:
    ```bash
    awk '{sum += $3} END {print sum}' data.txt
    ```
- Calculate the average salary
    ```bash 
    awk '{sum += $3; count++} END {print sum/count}' data.txt
    ```

#### Format output
```bash
    awk '{printf "Name: %s %s, Department: %s, Salary: $%d\n", $1, $2, $3, $4}' data.txt
```
#### Use Field Separators:

```bash 
    awk -F, '{print $1}' data.txt
```
#### Print lines where salary is greater than 6000:

```bash 
    awk '$3 > 6000' data.txt
```
#### Print the number of employees in each department:

```bash 
    awk '{dept[$2]++} END {for (d in dept) print d, dept[d]}' data.txt
```
#### Print Employees with Salaries Between 5000 and 7000

```bash
awk '$3 >= 5000 && $3 <= 7000 {print $1, $2, $3}' data.txt
```
### Buil In varaibles

- Print the Number of Lines in the File
    ```bash
    awk 'END {print "Number of lines:", NR}' data.txt
    ```