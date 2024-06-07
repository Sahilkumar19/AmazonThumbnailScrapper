# Amazon Product Thumbnail Scraper

This project is a Python script designed to scrape Amazon product pages to extract thumbnail images. It provides a convenient way to gather thumbnail URLs for multiple products and save them to a CSV file for further analysis or processing.

## Installation

1. Clone the repository to your local machine:

    ```bash
    git clone https://github.com/Sahilkumar19/amazon-product-thumbnail-scraper.git
    ```

2. Navigate to the project directory:

    ```bash
    cd amazon-product-thumbnail-scraper
    ```

3. Install the required dependencies using pip:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Prepare a CSV file containing a list of Amazon product links under the column name `ProductLink`.

2. Run the Python script `AmazonThumnails.py`:

    ```bash
    python AmazonThumbnails.py
    ```

3. The script will fetch thumbnail URLs for each product link and save them to a new CSV file named `thumbnails.csv`.

## CSV Format

The output CSV file `thumbnails.csv` will contain the following columns:

- `ProductLink`: The original Amazon product link.
- `Thumbnail_2`, `Thumbnail_3`, ...: URLs of the second, third, and subsequent thumbnails for each product.

Note: The script excludes the first thumbnail for each product link, as it often represents the main product image.

## Example

For example, if your input CSV file `products.csv` contains:

| ProductLink                                    |
|------------------------------------------------|
| https://www.amazon.com/product1               |
| https://www.amazon.com/product2               |

Running the script will generate an output CSV file `thumbnails.csv` with the following structure:

| ProductLink                                 | Thumbnail_2                                | Thumbnail_3                                |
|---------------------------------------------|--------------------------------------------|--------------------------------------------|
| https://www.amazon.com/product1            | https://example.com/thumbnail1_2.jpg    | https://example.com/thumbnail1_3.jpg    |
| https://www.amazon.com/product2            | https://example.com/thumbnail2_2.jpg    | https://example.com/thumbnail2_3.jpg    |

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

