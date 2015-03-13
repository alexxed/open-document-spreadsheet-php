This is a project offers support for handling spreadsheets in [OpenDocument](http://en.wikipedia.org/wiki/OpenDocument) format for PHP.

Currently, the library only offers basic write support and its main usage would be to export huge data to spreadsheets.

See the example.php file for a basic way of using it.

Try the pgsql2ods.php to run a query on your PostgreSQL server and export the results to a [OpenDocument](http://en.wikipedia.org/wiki/OpenDocument) spreadsheet.

An example:

`php pgsql2ods.php --file output.ods --server localhost --database test --user alex --password "" --port 5432 --query "SELECT * FROM client" && libreoffice output.ods`

The file is written directly to the disc, without using xml extensions, so you shouldn't have any problems with memory usage.

You also get a nice progress bar and if the database has any screwed up encoding, the broken characters will be stripped so that you can have a successful export.