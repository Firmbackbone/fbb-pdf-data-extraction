![FBB_Logo](https://firmbackbone.nl/wp-content/uploads/sites/694/2025/03/FBB-logo-wide.png)

**FIRMBACKBONE** is an organically growing longitudinal data-infrastructure with information on Dutch companies for scientific research and education. Once it is ready, it will become available for researchers and students affiliated with Dutch member universities through the Open Data Infrastructure for Social Science and Economic Innovations ([ODISSEI](https://odissei-data.nl/nl/)). FIRMBACKBONE is an initiative of Utrecht University ([UU](https://www.uu.nl/en)) and the Vrije Universiteit Amsterdam ([VU Amsterdam](https://vu.nl/en)) funded by the Platform Digital Infrastructure-Social Sciences and Humanities ([PDI-SSH](https://pdi-ssh.nl/en/front-page/)) for the period 2020-2025.

# fbb-pdf-data-extraction

This data extraction tool is designed to extract balance sheet information and profit & losses information from annual reports that are provided in PDF format. It is based on Jupyter Notebook and uses different approaches to achieve its goal. It uses MyMuPDF for when the textin the PDF files is accessible and uses OCR in case the text is not accessible (e.g. embedded in an image) and needs to be exted prior to processing it.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.

```bash
pip install foobar
```

## Usage

```python
import foobar

# returns 'words'
foobar.pluralize('word')

# returns 'geese'
foobar.pluralize('goose')

# returns 'phenomenon'
foobar.singularize('phenomena')
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
