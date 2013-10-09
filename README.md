jQuery.fixedTable
=================

A jQuery extension to fix headers within a table

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