# Easyvend API
Use this API if you want to make an comntainer compatible with vending and
depositing machines.

The API only has one function:

## `easyvend.register_chest = function(node_name, inv_list, meta_owner)`
Registers a node (called “chest”) for use with Easyvend. After calling this function,
the node will be recognized as storage for vending and depositing machines.

Easyvend makes the following assumptions about the chest:
* It has an inventory
* The inventory does not restrict the types of items you can put and take
* The chest is owned by a player
* The owner is specified in metadata

### Parameters 
* `node_name`: Name of the chest node
* `inv_list`: Name of the inventory list for exchanging items
* `meta_owner`: Identifier of the metadata variable storing the owner name

### Example
```
easyvend.register_chest("example:superchest", "main", "owner")
```
