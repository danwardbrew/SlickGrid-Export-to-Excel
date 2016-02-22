# Slickgrid Export to Excel
jQuery plugin to export the entire data from slick grid to excel. A client side javascript, jquery plugin to export slick grid to excel. 

## Get The Dashboard

* [Demo] (http://slick-excel-export.ranjithprabhu.in)

* [Download Source]  (https://github.com/ranjithprabhuk/SlickGrid-Export-to-Excel/archive/master.zip)

## Usage
* Include all the files inside the dist as it is in your application (dont call all js in your html page)
* Include require, underscore and jquery.slickgrid.export.excel js files in the html page

```
	<!-- add the following js files for Excel Exporting-->
    <script src="js/require.js"></script>
    <script src="js/underscore.js"></script>
    <script src="jquery.slickgrid.export.excel.js"></script>
```

* Configure the location of the js files as mentioned below
```
	<script>
		requirejs.config({
			baseUrl: '/examples/js'
		});
	</script>
```

* Now call the jquery plugin after building the slick grid

```
	<script>
		grid = new Slick.Grid("#myGrid", data, columns, options); // you will use this line to add your data to slick grid
		
		// after this line call the export to excel plugin
		$('body').exportToExcel("Report.xlsx", "Report", data, excelOptions, function (response) {
			console.log(response);
		});
	</script>
```
# Syntax for export to excel plugin
```
<script>
	$('body').exportToExcel(fileName.xlsx, excelWorksheetName, data, excelOptions, function (response) {
        console.log(response); // response gives base 64 content of the excel file name
    });
	
	fileName -> name of the file to be downloaded
	excelWorksheetName  -> name of the excel work sheet name
	data  -> same data parameter passed in Slick.grid
	excelOptions  -> option to format the cell styles and header styles
	callback() -> an call back function
</script>
```

## Plugins used
* require
* jsZip
* underscore
* swfobject
* excel builder



## About Author
* [Author URL] (http://ranjithprabhu.in)

I am passionate in playing with pixels, creating attractive designs which interact well with the user and love developing web apps. Have a good background in web design and development. Also having wonderful working experience with various interesting projects and participated in the development of the products to provide end to end solutions.


## License
Released under the MIT license.
