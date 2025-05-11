# fa
QUESTION 1
def modify_line(line):
    # Example modification: convert to uppercase
    return line.upper()

try:
    # Read from source file
    with open("input.txt", "r") as infile:
        lines = infile.readlines()

    # Modify content
    modified_lines = [modify_line(line) for line in lines]

    # Write to new file
    with open("output.txt", "w") as outfile:
        outfile.writelines(modified_lines)

    print("File processed successfully.")

except FileNotFoundError:
    print("Error: The input file was not found.")
except PermissionError:
    print("Error: Permission denied when accessing the file.")
except Exception as e:
    print(f"An unexpected error occurred: {e}")
QUESTION 2

def modify_line(line):
    # Example modification: strip whitespace and convert to uppercase
    return line.strip().upper() + '\n'

filename = input("Enter the name of the file to read: ")

try:
    with open(filename, "r") as infile:
        lines = infile.readlines()

    modified_lines = [modify_line(line) for line in lines]

    # Create output file name
    output_filename = "modified_" + filename

    with open(output_filename, "w") as outfile:
        outfile.writelines(modified_lines)

    print(f"Modified content written to {output_filename}.")

except FileNotFoundError:
    print(f"Error: File '{filename}' not found.")
except PermissionError:
    print(f"Error: Permission denied to read '{filename}'.")
except Exception as e:
    print(f"An unexpected error occurred: {e}")





