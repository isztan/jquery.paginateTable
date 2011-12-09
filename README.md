#PaginateTable

Takes a table full of rows and only displays a subset of rows a page at a time.
Responds to next page and previous page clicks to change the displayed page.
Displays total pages and current page. 
Hides pager if only a single page of rows.

##Demo

Try out a demo [here](http://jsfiddle.net/mattpage/n6jQX/11/)


##Example:
    
    <table id="myTable">
     <tbody>
        <tr><td>Apples</td></tr>
        <tr><td>Biscuits</td></tr>
        <tr><td>Cabbages</td></tr>
        <tr><td>Dumplings</td></tr>
        <tr><td>Eggs</td></tr>
        <tr><td>Flan</td></tr>
        <tr><td>Goose</td></tr>
        <tr><td>Ham</td></tr>
     <tbody>
    </table>
    <div class='pager'>
        <a href='#' alt='First' class='firstPage'>First</a>
        <a href='#' alt='Previous' class='prevPage'>Prev</a>
        
        <span class='currentPage'></span> of <span class='totalPages'></span>
        <a href='#' alt='Next' class='nextPage'>Next</a>
        <a href='#' alt='Last' class='lastPage'>Last</a>
    </div>
    
    <script>
    
    $(document).ready(function () {
        $('#myTable').paginateTable({ rowsPerPage: 2 });
    });
    </script>
    
    
Or if you would rather have page numbers instead of the previous/next links:
    
    <div class='pager'>
        <span class='pageNumbers'></span>
    </div>
    
Feel free to add rows to your tables. Just call paginateTable again. 
     
     var myTable = $('#myTable');
     myTable.paginateTable({ rowsPerPage: 2 }); 
     myTable.children('tbody').append('<tr><td>Hi</td></tr>');
     myTable.paginateTable({ rowsPerPage: 2 }); 

