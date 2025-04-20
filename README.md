# OrangeHRM Automation

This project is a test automation framework for the OrangeHRM application using Selenium and Pytest.

## Prerequisites

Before running the tests, ensure you have the following installed:

1. Python 3.7 or higher
2. Google Chrome browser
3. ChromeDriver (automatically managed by `chromedriver-autoinstaller`)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Tasheela99/orange-hrm-test-automation.git
   cd OrangeHRMAutomation
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Configuration

The application configuration is located in `Config.py`. Update the following variables as needed:
- `BASE_URL`: The URL of the OrangeHRM application.
- `USERNAME`: The username for login.
- `PASSWORD`: The password for login.
- `WAIT_TIME`: The maximum wait time for elements to load.
- `SLEEP_TIME`: The sleep time between actions.

## Running the Tests

1. To run all tests:
   ```bash
   pytest TestCases/TestOrangeHRM.py
   ```

## Logs and Screenshots

- Logs are saved in the `Logs` directory with a timestamped filename.
- Screenshots are saved in the `Screenshots` directory under a subfolder for each test run.

## Project Structure

```
OrangeHRMAutomation/
├── Config.py                # Configuration file
├── requirements.txt         # Python dependencies
├── conftest.py              # Pytest fixtures
├── Utilities/               # Utility modules (e.g., Logger)
├── PageObjects/             # Page Object Model classes
├── TestCases/               # Test case scripts
├── Logs/                    # Log files (auto-generated)
├── Screenshots/             # Screenshots (auto-generated)
└── README.md                # Project documentation
```

## Notes

- Ensure the Chrome browser version matches the ChromeDriver version managed by `chromedriver-autoinstaller`.
- Use the `--disable-warnings` flag with pytest to suppress warnings:
  ```bash
  pytest --disable-warnings
  ```

## License

This project is licensed under the MIT License.
