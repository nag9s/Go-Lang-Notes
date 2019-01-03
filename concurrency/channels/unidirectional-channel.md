To declare a unidirectional channel, you’ll simply include the &lt;- operator.

Readonly channel  \(receive channel\)\(Read Stream\)

&lt;-chan

roc := make\(&lt;-chan int\)

Sendonly Channel \(send channel\)\(write stream\)

chan&lt;-

soc := make\(chan&lt;- int\)

