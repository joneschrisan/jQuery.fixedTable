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
        jQuery('#myFixedTable').fixedTable({
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

    <table id="myFixedTable" class="fixedTable">
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

The above table format would produce the followint output:

    <div id="fixed_table_myFixedTable_container" style="height: 300px; width: 800px; clear: both;">
        <div id="fixed_table_myFixedTable_header" style="overflow: hidden; clear: both;">
            <div id="fixed_table_myFixedTable_header_first" style="float: left;">
                <table>
                    <tr>
                        <th>Column Header 1</th>
                    </tr>
                </table>
            </div>
            <div id="fixed_table_myFixedTable_header_headers" style="overflow: hidden; float: left; width: 527px;">
                <table id="fixed_table_myFixedTable_header_headers_table" style="width: 392px;">
                    <tr>
                        <th>Column Header 2</th>
                    </tr>
                    ...
                </table>
            </div>
            <div id="fixed_table_myFixedTable_header_last" style="float: left;">
                <table>
                    <tr>
                        <th>Column Header n</th>
                    </tr>
                </table>
            </div>
        </div>
        <div id="fixed_table_myFixedTable_table_content" style="clear: both; height: 248px;">
            <div id="fixed_table_myFixedTable_first" style="float: left; overflow: hidden; height: 248px;">
                <table>
                    <tr>
                        <th>Row 1 First Header</th>
                    </tr>
                    <tr>
                        <th>Row 2 First Header</th>
                    </tr>
                    ...
                    <tr>
                        <th>Row n First Header</th>
                    </tr>
                </table>
            </div>
            <div id="fixed_table_myFixedTable_table_body" style="float: left; overflow: auto; width: 527px; height: 248px;">
                <table id="fixed_table_myFixedTable_table_body_table" style="width: 392px;">
                    <tr>
                        <td>Row 1 Cell</td>
                    </tr>
                    <tr>
                        <td>Row 2 Cell</td>
                    </tr>
                    ...
                    <tr>
                        <td>Row n Cell</td>
                    </tr>
                </table>
            </div>
            <div id="fixed_table_myFixedTable_last" style="float: left; overflow: hidden; height: 248px;">
                <table>
                    <tr>
                        <th>Row 1 Last Header</th>
                    </tr>
                    <tr>
                        <th>Row 2 Last Header</th>
                    </tr>
                    ...
                    <tr>
                        <th>Row n Last Header</th>
                    </tr>
                </table>
            </div>
        </div>
        <div id="fixed_table_myFixedTable_footer" style="overflow: hidden; clear: both;">
            <div id="fixed_table_myFixedTable_footer_first" style="float: left;">
                <table>
                    <tr>
                        <th>Column Footer 1</th>
                    </tr>
                </table>
            </div>
            <div id="fixed_table_myFixedTable_footer_headers" style="overflow: hidden; float: left; width: 527px;">
                <table id="fixed_table_myFixedTable_footer_headers_table" style="width: 392px;">
                    <tr>
                        <th>Column Footer 2</th>
                    </tr>
                    ...
                </table>
            </div>
            <div id="fixed_table_myFixedTable_footer_last" style="float: left;">
                <table>
                    <tr>
                        <th>Column Footer n</th>
                    </tr>
                </table>
            </div>
        </div>
    </div>
