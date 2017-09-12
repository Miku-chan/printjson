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

- test.json::

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

 - Colorized indented::
 
        printjson test.json

- Minimized monochrome::

        printjson -om test.json

Result::
        
        {"test":"test","arr":[123,"λάμβδα ラムダ lambda",["1","2"]]}

Print third entry of "arr" array, using "__" as delimiter::

        printjson -k 'arr__2' -d '__' test3.json

Result::

        [
          "1",
          "2"
        ]



