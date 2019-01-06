ch &lt;- x // a send statement

x = &lt;-ch // a receive expression in an assignment statement

&lt;-ch  // a receive statement; result is discarded

![](/assets/import1.png)





case takeStream &lt;- &lt;-valueStream: // receive on valuestream\(uni directional  channel\) and send

