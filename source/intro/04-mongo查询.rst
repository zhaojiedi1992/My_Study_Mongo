mongo查询
=============================

and
-------------------------

.. code-block:: bash 

    db.col.find({key1:value1, key2:value2}).pretty()  

or
-------------------------

.. code-block:: bash 

    db.col.find( { $or: [ {key1: value1}, {key2:value2} ] } ).pretty()  

limit
---------------------------------

.. code-block:: bash 

    db.COLLECTION_NAME.find().limit(NUMBER)

skip
---------------------------------

.. code-block:: bash 

    db.COLLECTION_NAME.find().limit(NUMBER).skip(NUMBER)  

sort
-------------------------------------------------------

.. code-block:: bash 

    db.COLLECTION_NAME.find().sort({KEY:1}) 

聚合
------------------------------------------------------

.. code-block:: bash 

    db.mycol.aggregate([{$group : {_id : "$by_user", num_tutorial : {$sum : 1}}}]) 
