To declare a unidirectional channel, you’ll simply include the &lt;- operator.

Readonly channel  \(receive channel\)\(Read Stream\)  allows only **read operation**

&lt;-chan

roc := make\(&lt;-chan int\)

Sendonly Channel \(send channel\)\(write stream\) allow only **write operation **on them.

chan&lt;-

soc := make\(chan&lt;- int\)

