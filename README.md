![FBB_Logo](https://firmbackbone.nl/wp-content/uploads/sites/694/2025/03/FBB-logo-wide.png)

**FIRMBACKBONE** is an organically growing longitudinal data-infrastructure with information on Dutch companies for scientific research and education. Once it is ready, it will become available for researchers and students affiliated with Dutch member universities through the Open Data Infrastructure for Social Science and Economic Innovations ([ODISSEI](https://odissei-data.nl/nl/)). FIRMBACKBONE is an initiative of Utrecht University ([UU](https://www.uu.nl/en)) and the Vrije Universiteit Amsterdam ([VU Amsterdam](https://vu.nl/en)) funded by the Platform Digital Infrastructure-Social Sciences and Humanities ([PDI-SSH](https://pdi-ssh.nl/en/front-page/)) for the period 2020-2025.

# fbb-pdf-data-extraction

This data extraction tool is designed to extract balance sheet information and profit & losses information from annual reports that are provided in PDF format. 
It is based on Jupyter Notebook and can use different approaches to achieve its goal: 
- directly accessing text in the PDF files, and
- indirectly using OCR to recognize text in the PDF files prior to processing it.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install:
- openai
- langdetect
- pytesseract
- pdf2image
- Pillow
- pandas
- fitz
- pytesseract
- PIL
- sklearn
- numpy

```bash
pip install foobar
```

## Files Used

- The script processes a specific PDF file that needs to be specified
- The script uses an Excel sheet that contains the structure of the ledgers.
- Finally the financial_ledger.py contains all the names of ledgers that can be found in the PDF and to which group the script will assign them.

The General ledger structure is an Excel file that consist of the columns (exact):
| Hoofd posten code: | Postencode | Balans/res.rek. indicatie: | Debit/credit indicatie: | Omschr. postencode |
| ------------------ | ---------- | -------------------------- | ----------------------- | ------------------ |
| 100 | 110 | B | D | Non-material Assets |
| 100 | 120 | B | D | Material Assets |
| 100 | 130 | B | D | Financial Assets |
| 700 | 700 | R | D | Costs |
| 700 | 710 | R | D | Revenue Costs |
| 700 | 720 | R | D | Sales Costs |

The first column contains the ledger group code, the second column specifies a sub-group, the third column specifies whether the data should be listed on the balance sheet (B) or the profit and losses account (R), column four indicates debit (D) or credit (C) and the last column contains the ledger name.

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
