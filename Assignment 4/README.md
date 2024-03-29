# Assignment 4 : Database Management System

Similar to last Assignment, this time using Vector and Linked List to implement same database table. Use File input/output operations to retrieve table from file.

  -   C++ abstract class called AbstractDbTable
      -   rows()
      -   show()
      -   add()
      -   remove()
      -   get()
      -   loadCSV()   (non-virtual)
      -   saveCSV()   (non-virtual)
  -   C++ class called VectorDbTable that is a subclass of AbstractDbTable. Implement a database table using a vector.
  -   C++ class called LinkedListDbTable that is a subclassof AbstractDbTable. Implement a database table using a linked list data structure
  -   loadCSV() has input parameter (const char *infn) whichdenotes the file name of a comma-seperated value (CSV) file to be loaded. 
      -   Open file infn for reading
      -   Read all lines from infn. Add every line (which corresponds to a record) from the file into the table. If a line doesn't match expected format, the reading of the rest of the lines is terminated
      -   Close file
  -   saveCSV() has input parameter (const char *outfn) which denotes the file name to write to.
      -   Open file outfn for writing. File must be emptied.
      -   Write every record from the table into the file. A record must be written as a comma-separated value
      -   Close file
  -   main() function that accepts command line arguements. 
      -   Create instance of a database table (either VectorDbTable or LinkedListDbTable)
      -   Load CSV databade table file named default.csv
      -   If first command line arguement is 'showall', it will display all rows in the table
      -   if the first command line arguement is 'show', than it must be followed by a second command line arguement. The second arguement is the row number of the record to be displayed.
      -   Destroy instance of database table
