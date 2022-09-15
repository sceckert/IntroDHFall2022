# Contextual Note for NYC Knoedler Dataset

This data comes from Mathew Lincoln's discussion of the dataset used in his "[Critical Data Visualization with Palladio"](https://matthewlincoln.net/mapping-knoedler-palladio/#introduction-to-the-workshop-data0) tutorial.

Dataset downloaded from GitHub in January 2021

This folder includes CSV Lincoln generated from a larger dataset created by staff at the Getty working on the [Getty Provenance Index](https://www.getty.edu/research/tools/provenance/search.html) (a database of metadata about art sales and ownership). A larger set of data from the Knoedler stock books can be found here: [https://github.com/thegetty/provenance-index-csv/tree/main/knoedler#knoedler-stock-books](https://github.com/thegetty/provenance-index-csv/tree/main/knoedler#knoedler-stock-books)

From Lincoln's description in the "Critical Data Visualization with Palladio" tutorial:

> " These data describe a little over 4,100 sales by the fine art dealer M. Knoedler & Co. between roughly 1870-1970, as documented in data encoded from the handwritten stockbooks by staff at the Getty Provenance Index. These stockbooks were where Knoedler recorded details about the artworks that entered their inventory, when and where they bought them from and for how much, and (if sold) who the eventual buyer was."

> The data in nyc_knoedler.csv covers only those cases in which:
> > 1. The transactions were actually recorded in the Knoedler stockbooks (they didn’t always keep good records!)
> > 2. The records contain original purchase and sale dates and prices.
> > 3. We have been able to identify both the buyer and the seller.
> > 4.  The buyer has a known street address located in Manhattan or Brooklyn (i.e. if our only location info says “New York, NY”, it is not included in this subset because it doesn’t contain street-level precision." 


## Data dictionary (by Matthew Lincoln)


| field                | description                                                                                                                                                                                                                                                                                 |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `title`              | Title of the work (if recorded)                                                                                                                                                                                                                                                             |
| `artists`            | Creator(s) of the artwork (if recorded. GPI edtiors recorded the original spelling as written by Knoedler, but also recorded a standardized version if they could identify the artist [e.g. turning "J. Sargent" into "SARGENT, JOHN SINGER"]. This field holds the standardized versions.) |
| `artist_nationality` | Creator(s) nationalities (input by modern editors)                                                                                                                                                                                                                                          |
| `genre`              | Genre of the work (input by modern editors)                                                                                                                                                                                                                                                 |
| `object_type`        | e.g. `Painting`, `Drawing`, `Sculpture` (input by modern editors)                                                                                                                                                                                                                           |
| `height`             | Height in inches (if recorded)                                                                                                                                                                                                                                                              |
| `width`              | Width in inches (if recorded)                                                                                                                                                                                                                                                               |
| `area`               | Area in square inches (if recorded)                                                                                                                                                                                                                                                         |
| `seller`             | Name of seller (Standardized in a similar manner to the artists. Numeric ID if anonymous/unknown)                                                                                                                                                                                           |
| `seller_type`        | e.g. `Dealer`, `Museum`, `Artist`, `Collector`                                                                                                                                                                                                                                              |
| `buyer`              | Name of buyer (Standardized in a similar manner to the artists. Numeric ID if anonymous/unknown)                                                                                                                                                                                            |
| `buyer_type`         | e.g. `Dealer`, `Museum`, `Artist`, `Collector`                                                                                                                                                                                                                                              |
| `buyer_address`      | Buyer address                                                                                                                                                                                                                                                                               |
| `coordinates`        | Coordinates in the format `lat,lon`                                                                                                                                                                                                                                                         |
| `purchase_date`      | Date object brought into Knoedler stock in the format `YYYY-MM-DD`                                                                                                                                                                                                                          |
| `sale_date`          | Date object sold out of Knoedler stock in the format `YYYY-MM-DD`                                                                                                                                                                                                                           |
| `purchase_price`     | Price Knoedler paid to buy the object (normalized to 1900 USD)                                                                                                                                                                                                                              |
| `sale_price`         | Price Knoedler received for selling the object (normalized to 1900 USD)                                                                                                                                                                                                                     |
