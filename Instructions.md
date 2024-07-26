# Scavenger

## Overview
`scavenger` is a command-line tool that recursively scrapes websites and outputs their content in markdown format.

## Installation
1. Make sure you have Go installed on your machine.
2. Clone the repository or download the source code.
3. Run `go build -o scavenger` to build the binary.

## Usage


## Flags
- `--config` (default is `$HOME/.scavenger.yaml`): Path to the config file.
- `--start-url` (required): The URL to start scraping from.
- `--max-depth` (default is `3`): Maximum depth for recursive scraping.
- `--concurrent-requests` (default is `5`): Number of concurrent requests.
- `--output-path` (default is current directory): Path to save the scraped markdown files.
- `--scrape-external` (default is `false`): Whether to scrape external links.
- `--external-depth` (default is `1`): Maximum depth for external link scraping.

## Examples
Start scraping with a maximum depth of 2 and saving the output to the `output` directory:

`scavenger --start-url "http://example.com" --max-depth 2 --output-path "./output"`


Scrape with concurrent requests set to 10:

`scavenger --start-url "http://example.com" --concurrent-requests 10`


Scrape external links up to a depth of 1:

`scavenger --start-url "http://example.com" --scrape-external --external-depth 1`


## Configuration File
The configuration file is an optional YAML file. The default location is `$HOME/.scavenger.yaml`.

Example configuration file:
```yaml
start_url: "http://example.com"
max_depth: 3
concurrent_requests: 5
output_path: "./output"
scrape_external: false
external_depth: 1
```

## Graceful Shutdown
 
The scraper handles interrupt signals (Ctrl+C) gracefully, ensuring that ongoing scrapes are completed before the program exits.
 
## Logging
 
All errors and important information are logged to the console.
 
## Output
 
Scraped content is saved as markdown files in the specified output directory. External links are saved in a markdown file named external_links.md in the output directory.
 
## License
 
This project is licensed under the MIT License.