ch := make\(chan int\) // unbuffered channel

ch &lt;- 12 // blocks

fmt.Println\(&lt;-ch\) // read from the channel
