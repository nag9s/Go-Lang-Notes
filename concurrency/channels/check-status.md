goroutine can find out state of the channel using val, ok := &lt;- channel syntax where ok is true if channel is open or read operations can be performed and false if channel is closed and no more read operations can be performed.

