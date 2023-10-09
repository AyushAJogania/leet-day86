# leet-day86

# Single Number Finder

This program is designed to find the single number in an array of integers where all other elements appear twice. The solution provided uses XOR operation to achieve this with a linear runtime complexity and constant extra space.

## Usage

1. Clone the repository or download the source code.

2. Compile the source code using a C++ compiler:

   ``
   g++ -o single_number_finder single_number_finder.cpp
   ```

3. Run the program:

      ./single_number_finder
   

4. Input your array of integers when prompted.

5. The program will return the single number that appears only once in the array.

## Example

### Input

```
Enter the array of integers separated by spaces: 4 1 2 1 2
```

### Output

```
Single number: 4
```

## Constraints

- The input array `nums` should contain integers.
- The length of `nums` should be between 1 and 3 * 10^4.
- The values of the integers in `nums` should be between -3 * 10^4 and 3 * 10^4.

