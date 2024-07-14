# Fixed Width File Parser

This project parses a fixed-width file into a CSV file based on a specified format.

## Files

- `spec.txt`: Specification file defining the lengths of each field.
- `data.txt`: Sample fixed-width data file to be parsed.
- `fixed_width_parser.py`: Python script to parse the fixed-width file and generate a CSV file.
- `Dockerfile`: Docker configuration to run the parser in a container.

## Usage

### Run with Python Job Local

1. Ensure you have Python3 installed.
2. Set Python path by using: 
  ```sh
  $env:PATH += ";C:\Users\<YourUsername>\AppData\Local\Programs\Python\Python<version>\"
3. Run the script:
   ```sh
   python fixed_width_parser.py


### Run Python Job using Docker Container

1. Build docker Image:
   ```sh
    docker build -t image-name .
2. Run Docker Image:
   ```sh
   docker run image-name
3. Mount generated output.csv file
   ```sh
   docker run -v ${PWD}:/app -w /app image-name

