# Map Application

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A simple web page demonstrating the `<csv-map>` web component, which displays locations from CSV data on an interactive map.

## Demo

- **[Live Demo](https://code4fukui.github.io/map/)**
- [Blog post (Japanese)](https://fukuno.jig.jp/3277)

## Features

- **Easy to Use**: Displays a map by simply adding a `<csv-map>` HTML tag.
- **CSV Powered**: Populates map markers directly from inline CSV data.
- **Interactive Popups**: Shows location details (name, photo, and link) when a marker is clicked.
- **Geo3x3 Support**: Uses the [geo3x3](https://github.com/code4fukui/geo3x3-js) format for precise location encoding.

## Usage

To add a map to your HTML page, follow these two steps:

1.  **Include the script**
    Add the `csv-map.js` module to the `<head>` of your HTML file.

    ```html
    <script type="module" src="https://code4fukui.github.io/csv-map/csv-map.js"></script>
    ```

2.  **Add the `<csv-map>` element**
    Place the `<csv-map>` element in your `<body>` and fill it with your location data in CSV format. The first line must be the header.

    ```html
    <csv-map>
    name,url,geo3x3,photo
    Yokogawa Bunten,https://volga-rice.jimdofree.com/,,volga-yokogawa.jpg
    Sun Dome Fukui,http://www.sankan.jp/sundome/,E9138732236,
    Fukui National College of Technology,https://www.fukui-nct.ac.jp/,E9138732251953,
    </csv-map>
    ```

### CSV Format

The component requires a header row and subsequent rows with data for each location.

-   `name`: (Required) The name of the location, displayed in the popup.
-   `url`: (Optional) A URL to link to from the popup.
-   `geo3x3`: (Required) The location's coordinates in `geo3x3` format. Rows without a `geo3x3` value will not be displayed on the map.
-   `photo`: (Optional) A URL or relative path to an image for the location.

## License

This project is available under the [MIT License](LICENSE).