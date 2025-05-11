# fa
QUESTION 1

    # Read from source file
    with open("input.txt", "r") as infile:
        lines = infile.readlines()

    # Modify content
    modified_lines = [modify_line(line) for line in lines]

    # Write to new file
    with open("output.txt", "w") as outfile:
        outfile.writelines(modified_lines)

    print("File processed successfully.")


QUESTION 2


    with open(filename, "r") as infile:
        lines = infile.readlines()

    modified_lines = [modify_line(line) for line in lines]

    # Create output file name
    output_filename = "modified_" + filename

    with open(output_filename, "w") as outfile:
        outfile.writelines(modified_lines)

    print(f"Modified content written to {output_filename}.")







