# info-664-final

This program was designed to take the Cooper Hewitt, Smithsonian Design Museum's entire object collections CSV list and parse it using the Pandas open source library.

The refined source file is located here: https://drive.google.com/file/d/1eA8UXPpAK_LgKF0yJ4tTlJlAel-EE_rY/view?usp=sharing

The original CSV file was pulled from Cooper Hewitt's GitHub here: https://github.com/cooperhewitt/collection/blob/master/meta/objects.csv

I refined this CSV file using OpenRefine with the following edits:
1. Clustered and edited cells in the 'date' and 'type' columns to collapse similar yet slightly varied values into one value. I relied on the "Key collision" method and the "Fingerprint" keying function to find clusters to compile in these columns.
2. I ran cell transformation on the "medium", "type" and "date" using the following Grel function to capitalize the first letter in the cell: "grel:toUppercase(substring(value,0,1 ))+toLowercase(substring(value,1))" This was sourced from this tutorial: https://geospatialmetadatalibrarian.blogspot.com/2017/01/more-cleaning-up-keywords-in-openrefine.html

These changes hopefully increased the number of similar group values populating from my code, thus increasing the number of matching records.
