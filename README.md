# Bambulabs API

This package provides a Python API for interacting with BambuLab 3D Printers. The API enables you to control and monitor your printer programmatically, making it an essential tool for developers, makers, and automation enthusiasts. The project is open-source and available on PyPI.

## Status

[![flake8](https://github.com/mchrisgm/bambulabs_api/actions/workflows/flake8.yml/badge.svg)](https://github.com/mchrisgm/bambulabs_api/actions/workflows/flake8.yml)
[![pytest-unit-tests](https://github.com/mchrisgm/bambulabs_api/actions/workflows/pytest-unit-tests.yml/badge.svg)](https://github.com/mchrisgm/bambulabs_api/actions/workflows/pytest-unit-tests.yml)
[![GitHub Pages](https://github.com/mchrisgm/bambulabs_api/actions/workflows/static.yml/badge.svg)](https://github.com/mchrisgm/bambulabs_api/actions/workflows/static.yml)

## Documentation

Comprehensive documentation for this package, including API reference and usage guides, can be found [here](https://mchrisgm.github.io/bambulabs_api/).

## Installation

To install the package, use `pip`:

```bash
pip install bambulabs_api
```

Make sure you have Python 3.6 or higher installed.

## Features

- **Connect and control** BambuLab 3D printers programmatically.
- **Monitor printer status** in real-time.
- **Execute commands** and manage print jobs directly through Python code.
- **Easy setup** and integration with Python environments.

## Usage Example

Below is a basic example demonstrating how to connect to a BambuLab 3D printer and retrieve its status using the API:

```python
import bambulabs_api as bl

IP = '192.168.1.200'
SERIAL = 'AC12309BH109'
ACCESS_CODE = '12347890'

if __name__ == '__main__':
    print('Starting bambulabs_api example')
    print('Connecting to BambuLab 3D printer')
    print(f'IP: {IP}')
    print(f'Serial: {SERIAL}')
    print(f'Access Code: {ACCESS_CODE}')

    # Create a new instance of the API
    printer = bl.Printer(IP, ACCESS_CODE, SERIAL)

    # Connect to the BambuLab 3D printer
    printer.connect()

    # Get the printer status
    status = printer.get_state()
    print(f'Printer status: {status}')

    # Disconnect from the BambuLab 3D printer
    printer.disconnect()
```

## Development

If you want to contribute to the development of this API or run it in a development environment, follow these steps:

### Prerequisites

- **Conda**: Make sure you have Conda installed on your system.
- **Git**: Ensure Git is installed for cloning the repository.

### Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/mchrisgm/bambulabs_api.git
   ```

2. Change directory:

   ```bash
   cd bambulabs_api
   ```

3. Create the Conda environment using the provided `environment.yml` file:

   ```bash
   conda env create -f environment.yml
   ```

4. Activate the environment:

   ```bash
   conda activate blapi
   ```

5. Install the package in development mode:

   ```bash
   pip install -e .
   ```

### Running Tests

To ensure everything is working correctly, you can run the tests using `pytest`:

```bash
pytest
```

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

Please make sure your code follows PEP 8 guidelines and that you run tests before submitting a PR.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Support

If you encounter any issues or have questions, feel free to open an issue on the [GitHub repository](https://github.com/mchrisgm/bambulabs_api/issues).

## Acknowledgements

This package is an open-source project developed and maintained by the community. Special thanks to all contributors who have helped improve and enhance this API.
