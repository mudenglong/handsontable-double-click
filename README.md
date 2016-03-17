# Handsontable double click

A Handsontable plugin allow observe dblClick event.

## Installation

```bash
bower install --save handsontable-double-click
```

## Usage

```html
<!DOCTYPE html>
<html lang='en'>
  <head>
    <meta charset='UTF-8'>
    <title>Handsontable Select Plus</title>
    <link rel='stylesheet'
      href='bower_components/handsontable/dist/handsontable.full.css'>
    <script src='bower_components/handsontable/dist/handsontable.full.js'></script>
    <script src='handsontable-double-click.js'></script>
  </head>
  <body>
    <div id='example'></div>
    <pre id='logs'></pre>
    <script>
      var log = function (message) {
        let logs = document.getElementById('logs');
        logs.appendChild(document.createTextNode(message + '\n'));
      };
      var container = document.getElementById('example');
      var hot = new Handsontable(container, {
        colHeaders: true,
        rowHeaders: true,
        dblClick: function (row, col) {
          log('dbClick  ' + row + ' ' + col);
        },
        dblClickCell: function (row, col) {
          log('dbClickCell ' + row + ' ' + col);
        },
        dblClickColHeader: function (col) {
          log('dblClickColHeader ' + col);
        },
        dblClickRowHeader: function (row) {
          log('dblClickRowHeader ' + row);
        },
        dblClickCorner: function (row, col) {
          log('dblClickConner ' + row + ' ' + col);
        }
      });
    </script>
  </body>
</html>
```

## Example

```bash
git clone https://github.com/vn38minhtran/handsontable-double-click.git
cd handsontable-double-click
npm install && bower install
npm start
```