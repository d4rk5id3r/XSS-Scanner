# XSS Scanner using Python

This Python script demonstrates a simple Cross-Site Scripting (XSS) scanner. It can be used to detect XSS vulnerabilities in web forms within a given URL. 

## Requirements
- Python 3.x
- `requests` library
- `BeautifulSoup` library (`bs4`)

## Installation
1. Ensure you have Python 3.x installed on your system.
2. Install the required libraries using pip:
   ```bash
   pip install requests
   pip install beautifulsoup4

## Usage

1. Clone or download the script from the repository.
2. Import the necessary libraries:

    ```python
    import requests
    from pprint import pprint
    from bs4 import BeautifulSoup as bs
    from urllib.parse import urljoin
    ```

3. Define the following functions:
   - `get_all_forms(url)`: Retrieves all forms present in the specified URL.
   - `get_form_details(form)`: Extracts details such as action, method, and inputs from a form.
   - `submit_form(form_details, url, value)`: Submits a form with a provided value for testing XSS vulnerability.
   - `scan_xss(url)`: Scans the specified URL for XSS vulnerabilities.

4. Execute the `scan_xss(url)` function, passing the URL you want to scan as a parameter.

   Example usage:

    ```python
    if __name__ == "__main__":
        url = "https://example.com"
        print(scan_xss(url))
    ```

   Replace `"https://example.com"` with the URL you want to scan.

## Example

An example script usage is provided to demonstrate how to scan a URL for XSS vulnerabilities. In this example, the script is used to scan the URL `"https://xss-game.appspot.com/level1/frame"`.

```python
if __name__ == "__main__":
    url = "https://xss-game.appspot.com/level1/frame"
    print(scan_xss(url))
