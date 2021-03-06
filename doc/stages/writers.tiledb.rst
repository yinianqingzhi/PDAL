.. _writers.tiledb:

readers.tiledb
==============

Implements `TileDB`_ 1.4.1+ reads from an array.

.. plugin::

Example
-------

.. code-block:: json

  {
    "pipeline":[
      {
        "type":"readers.las",
        "array_name":"input.las"
      },
      {
        "type":"writers.tiledb",
        "array_name":"output_array"
      }
    ]
  }


Options
-------

array_name
`TileDB`_ array to write to. [Required]

config_file
`TileDB`_ configuration file [Optional]

tile_data_capacity
Number of points per tile [Optional]

x_tile_size
Tile size (x) in a Cartesian projection [Optional]

y_tile_size
Tile size (y) in a Cartesian projection [Optional]

z_tile_size
Tile size (z) in a Cartesian projection [Optional]

compression
TileDB compression type for attributes, default is None [Optional]

compression_level
TileDB compression level for chosen compression [Optional]

stats
Dump query stats to stdout [Optional]


.. include:: writers_opts.rst

.. _TileDB: https://tiledb.io
