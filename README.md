# Map Application

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A simple map application that displays locations from a CSV file.

## Demo
[Try the demo](https://code4fukui.github.io/map/)

## Features
- Displays locations on a map using CSV data
- Supports geo3x3 format for location data
- Displays photos for each location

## Usage
1. Ensure you have a CSV file with the following format:
   - Name, URL, geo3x3, photo
2. Include the `csv-map.js` script in your HTML file:
   ```html
   <script type="module" src="https://code4fukui.github.io/csv-map/csv-map.js"></script>
   ```
3. Add a `<csv-map>` element to your HTML and populate it with the CSV data:
   ```html
   <csv-map>
   名前,URL,geo3x3,photo
   ヨコガワ分店,https://volga-rice.jimdofree.com/,,volga-yokogawa.jpg
   サンドーム福井,http://www.sankan.jp/sundome/,E9138732236,
   福井高専,https://www.fukui-nct.ac.jp/,E9138732251953,
   </csv-map>
   ```

## License
This project is licensed under the MIT License.