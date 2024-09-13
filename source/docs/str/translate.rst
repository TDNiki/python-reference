=========
translate
=========

Description
----------
Returns a copy of the string with characters mapped through the given translation table or deleted.

Syntax
------
**str**. *translate(table[, deletechars])*

*table*
    Required. Must be a string of length 256.
*deletechars*
    Optional. Characters to be deleted from the string.

Return Value
------------
**str**

Time Complexity
---------------
#TODO

Remarks
-------
You can use the **maketrans()** helper function in the **str** object to create a translation table.

Example 1
---------
>>> # this example deletes all the vowels from the string
>>> "ABCDE".translate(''.maketrans('', '', "AEIOU"))
'BCD'

Example 2
---------
>>> translation_table = ''.maketrans('aeiou', '!@#$%')
>>> translation_table   # note the replaced vowels
{97: 33, 101: 64, 105: 35, 111: 36, 117: 37}
>>> translation_table = ''.maketrans('AEIOU', '!@#$%')
>>> "ABCDE".translate(translation_table)
'!BCD@'


See Also
--------
#TODO
