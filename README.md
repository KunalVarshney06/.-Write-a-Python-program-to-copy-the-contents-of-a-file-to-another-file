# .-Write-a-Python-program-to-copy-the-contents-of-a-file-to-another-file
def copy_file(source_path, destination_path):
    try:
        with open(source_path, 'r') as source_file:
            with open(destination_path, 'w') as destination_file:
                for line in source_file:
                    destination_file.write(line)
        print("File copied successfully.")
    except FileNotFoundError:
        print("Source file not found.")
    except IOError:
        print("An error occurred while copying the file.")

# Example usage
source_file_path = 'path/to/your/source_file.txt'  # Replace with the actual source file path
destination_file_path = 'path/to/your/destination_file.txt'  # Replace with the actual destination file path
copy_file(source_file_path, destination_file_path)
