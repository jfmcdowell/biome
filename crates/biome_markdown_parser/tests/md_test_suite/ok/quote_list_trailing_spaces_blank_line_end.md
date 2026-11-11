<!-- No .html sidecar: a quote line with only whitespace after ">" still renders as an empty paragraph inside the quote, so these cases cannot be compared with reference HTML yet. The CST snapshot covers them: each inner list item ends before the whitespace-only quote line, which keeps the lists tight. -->

- > - a
  >   

***

- > - a
  >   
- b

***

> - a
>   

***

- > > - a
  > >   

***

- > - a
  >   
  >   
- b

***

- > - a
  >	  
