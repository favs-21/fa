# fa

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
