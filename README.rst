Utility for pretty JSON output
==============================

Simple python utility for using in shell scripts.

Features
--------

- Print colorized JSON
- Minimized and formatted output
- Output elements by keys and indexes
- Check JSON for correctness
- Automatically disabling color sequences, when prints to pipeline, file or other non-tty output

Examples
--------

- test.json
 
.. code:: json

        {
          "arr": [
            123,
            "λάμβδα ラムダ lambda",
            [
              "1",
              "2"
            ]
          ],
          "test": "test"
        }


 - Colorized indented
 
.. code:: bash
 
        printjson test.json

- Minimized monochrome
 
.. code:: bash
 
        printjson -om test.json

Result:
 
.. code:: json
 
        {"test":"test","arr":[123,"λάμβδα ラムダ lambda",["1","2"]]}

- Print third entry of "arr" array, using "__" as delimiter

.. code:: bash

        printjson -k 'arr__2' -d '__' test3.json

Result:

.. code:: json

        [
          "1",
          "2"
        ]



