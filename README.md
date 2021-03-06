FACTORY I/O (SDK)
=================

With the SDK, developers can integrate FACTORY I/O with virtually anything. It provides tools so that you can develop interfaces between FACTORY I/O and any type of external technologies. Included in the SDK is the Engine I/O assembly, Engine I/O Explorer tool and several samples so you can get started right away.

Engine I/O
----------

Engine I/O is a .NET 2.0 assembly for inter-process communication (IPC) between FACTORY I/O and custom applications. It gives access to the simulation I/O points through a memory mapped file. The memory is divided in three groups: Inputs, Outputs and Memories. Standing from a controller point of view, Inputs are used to read sensors values, Outputs to write actuators and Memories to exchange generic data. An I/O point is made of a memory address, name and value representing a specific data type.

Some considerations to take into account when using Engine I/O:

* The MemoryMap class is a singleton, meaning that only one instance can exist. This instance represents a cached copy of the memory mapped file.
* The MemoryMap.Instance.Update() method is responsible for synchronizing cached data with the actual memory. This method must be called every time there is the need to read/write the latest I/O points or receive event notifications.

Engine I/O Explorer Tool
------------------------

The Engine I/O Explorer is a tool developed to browse I/O points addresses, names and values. It can be used to observe or force I/O points values, whether they are Inputs, Outputs or Memories.
