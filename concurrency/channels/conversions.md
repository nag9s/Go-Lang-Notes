 Conversions from bidirectional to unidirectional channel types are permitted in any assignment. There is no going back, however: once you have a value of a unidirectional type such as 

`chan <- int`

, there is no way to obtain from it a value of type 

`chan int`

 that refers to the same channel data structure.

