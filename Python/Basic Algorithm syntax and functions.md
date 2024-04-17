
### range()

1. **range(stop)**:
    
    - `stop`: The value at which to stop generating numbers (this value is not included in the sequence).
    - Example: `range(5)` generates numbers from 0 to 4.
2. **range(start, stop)**:
    
    - `start`: The starting value of the sequence (this value is included in the sequence).
    - `stop`: The value at which to stop generating numbers (this value is not included in the sequence).
    - Example: `range(1, 5)` generates numbers from 1 to 4.
3. **range(start, stop, step)**:
    
    - `start`: The starting value of the sequence (this value is included in the sequence).
    - `stop`: The value at which to stop generating numbers (this value is not included in the sequence).
    - `step`: The difference between each number in the sequence (the amount by which to increase or decrease).
    - Example: `range(1, 10, 2)` generates numbers 1, 3, 5, 7, and 9.


### hash()

1. **only for immutable
	- `hash()` is only work with immutable object such as  tuple, string
	- not work with mutable object such as list, dict
2. **guarateed equality
	- immutalbe objects with the same value always return the same hash value
	- this ensures that the same object will have the same hash value at different parts of the program or at different run times. 