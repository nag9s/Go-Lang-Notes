ch := make\(chan int\) // unbuffered channel

ch &lt;- 12 // blocks   // write to the channel

fmt.Println\(&lt;-ch\) // read from the channel

