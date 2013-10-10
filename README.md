jQuery.fixedTable
=================

A jQuery extension to fix headers within a table


    Table header tags will be fixed.
    
    Column headers must be within the <thead> tag.
    Column footers must be within the <tfoot> tag.
    Row headers must still be <th> tags but must be within the <tbody> tag
    
    The table must have an id attribute.


Example 1 (Individual Table):

    jQuery(document).ready(function() {
        jQuery('#table_0').fixedTable({
            table: {
                height: 300,
                width: 800
            }
            
        });
    });
 
Example 2 (All Tables With Class Name):

    jQuery.fixedTableByClassName('fixedTable', {
        table: {
                height: 300,
                width: 800
            }
            
        });
    });

Table format (n refers to any number) (Fixed Header, Fixed First Column, Fixed Last Column, Fixed Footer):

    <table id="myFixedTable">
        <thead>
            <tr>
                <th>Column Header 1</th>
                <th>Column Header 2</th>
                ...
                <th>Column Header n</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th>Row 1 First Header</th>
                <td>Row 1 Cell</td>
                ...
                <th>Row 1 Last Header</th>
            </tr>
            <tr>
                <th>Row 2 First Header</th>
                <td>Row 2 Cell</td>
                ...
                <th>Row 2 Last Header</th>
            </tr>
            ...
            <tr>
                <th>Row n First Header</th>
                <td>Row n Cell</td>
                ...
                <th>Row n Last Header</th>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <th>Column Footer 1</th>
                <th>Column Footer 2</th>
                ...
                <th>Column Footer n</th>
            </tr>
        </tfoot>
    </table>
